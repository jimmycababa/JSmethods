JS Methods

Map - a map object iterates its elements in insertion order. It creates a new array populated with the results of calling a provided function on every element in the calling array. It allows us to transform each element of an array, with affecting the orginal array. 

examples
1. const myArray = [1, 2, 3];
// Multiply each element x 2
const myMappedArray = myArray.myMap(e => e * 2)
console.log(myMappedArray) // [2, 4, 6];

2. const array1 = [1, 4, 9, 16];
// pass a function to map
const map1 = array1.map(x => x * 2);
console.log(map1);
// expected output: Array [2, 8, 18, 32]

3. function invert(array) {
 return array.map(x => -x)
  }

  Reduce - a function that folds a list into any data type. it's like folding a box and you can turn an array [1,2,3,4,5] into the number 15 by adding them all up. it takes two parameters (the reducer and an initial value). accumulator is the eventual return value.

  examples
  1. const add = (x, y) => x + y;
const numbers = [1, 2, 3, 4, 5];

numbers.reduce(add);
// 15

2. function average(scores) {
  let answer = scores.reduce((a,c) => a + c,0);
   return Math.round(answer / scores.length)
}

3. function avg(a){
  let sum = a.reduce((a,c) => a + c, 0)
  return sum/a.length
}

filter - this method takes an array as an input. it takes each element in the array and it applies a conditional statement against it. if this conditional returns true, the element gets 'pushed' to the output array. once each element in the input array is 'filtered' as such, it outputs a new array containing each element that returned true.

examples

1. var numbers = [1, 3, 6, 8, 11];

var lucky = numbers.filter(function(number) {
  return number > 7;
});

// [ 8, 11 ]

2. const numbers = [1, 2, 3, 4];
const evens = numbers.filter(item => item % 2 === 0);
console.log(evens); // [2, 4]

3. function isBigEnough(value) {
  return value >= 10
}

let filtered = [12, 5, 8, 130, 44].filter(isBigEnough)
// filtered is [12, 130, 44]

forEach - this method passes a callback function for each element of an array together with the following parameters:
current value (required) - the value of the current array element
index (optional) - the current elements index number
array (optional) - the array object to which the current element belongs

examples

1. const numbers = [1, 2, 3, 4, 5];
numbers.forEach(function(number) {
    console.log(number);
});

2. const items = ['item1', 'item2', 'item3']
const copyItems = []
items.forEach(function(item){
  copyItems.push(item)
})

3. const arr = [1, 'two',];
arr.forEach(item => console.log(item));
// Expected output:
// 1 
// two

sort - this method converts each item in the array into strings and constructs the sequence by comparing each array item based on the UTF-16 code valies when there is no callback specified. UTF-16 is the standardized form for translating bits into a format comprehensible to humans. its basically a translation table for a corresponding character.

examples
1. const teams = ['Real Madrid', 'Manchester Utd', 'Bayern Munich', 'Juventus'];
teams.sort(); 

// ['Bayern Munich', 'Juventus', 'Manchester Utd', 'Real Madrid']

2. const numbers = [3, 23, 12];

numbers.sort(); // --> 12, 23, 3

3. const numbers = [3, 23, 12];

numbers.sort(function(a, b){return b - a}); // --> 23, 12, 3

slice - this method copies a given part of an array and returns that copied part as a new array. it doesnt change the orginal array. it does not include the last given element.

examples
1. let fruits = ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango']
let citrus = fruits.slice(1, 3)

// fruits contains ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango']
// citrus contains ['Orange','Lemon']

2. var colors = ['red','green','blue','yellow','purple'];
var rgb = colors.slice(0,3);
console.log(rgb); // ["red", "green", "blue"]

3. var a = [1,2,3,4,5];
a.slice(0,3);    // Returns [1,2,3]
a.slice(3);      // Returns [4,5]
a.slice(1,-1);   // Returns [2,3,4]

pop - this method removes the last element from an array and returns that element, which changes the length of the array. if you call pop on an empty array it returns undefined. 

examples
1. var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];

var popped = myFish.pop();

console.log(myFish); // ['angel', 'clown', 'mandarin' ]

console.log(popped); // 'sturgeon'

2. var languages = ["JavaScript", "Python", "Java", "C++", "Lua"];

var popped = languages.pop();

console.log(languages); // [ 'JavaScript', 'Python', 'Java', 'C++' ]

3. let cats = ['Bob', 'Willy', 'Mini'];

cats.pop(); // ['Bob', 'Willy']

shift - this method removes the first element from an array and returns that removed element. this method changes the length of the array.

examples
1. var languages = ["JavaScript", "Python", "Java", "C++", "Lua"];

var shifted = languages.shift();

console.log(languages); // [ 'Python', 'Java', 'C++', 'Lua' ]

2. let apps = ["Instagram", "Facebook", "Messanger"];
apps.shift();

console.log(apps);

3. let names = ["Harvey", "Donna", "Mike", "Rachel" ,"Louis", "Jessica"];

while( (i = names.shift()) !== undefined ) {
    console.log(i);
}

push - this method add one or more elements to the end of an array and returns the new length of the array.

examples
1. const animals = ['pigs', 'goats', 'sheep'];
const count = animals.push('cows');
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows"]

2. let sports = ['soccer', 'baseball']
let total = sports.push('football', 'swimming')

console.log(sports)  // ['soccer', 'baseball', 'football', 'swimming']

3. let vegetables = ['parsnip', 'potato']
let moreVegs = ['celery', 'beetroot']

// Merge the second array into the first one
// Equivalent to vegetables.push('celery', 'beetroot')
Array.prototype.push.apply(vegetables, moreVegs)

console.log(vegetables)  // ['parsnip', 'potato', 'celery', 'beetroot']

unshift - this method adds one or more elements to the beginning of an array and returns the new length of the array.

examples
1. const array1 = [1, 2, 3];
console.log(array1);
// expected output: Array [4, 5, 1, 2, 3]

2. let apps = ["Instagram", "Facebook", "Messanger"];
apps.unshift("Oculus", "WhatsApp");

console.log(apps);

3. let arr = [1, 2];

arr.unshift(0); // result of call is 3, the new array length
// arr is [0, 1, 2]

includes - this method determines whether an array includes a certain value among its entries, returning true or false as appropriate.

examples 
1. const array1 = [1, 2, 3];

console.log(array1.includes(2));
// expected output: true

2. var totn_string = 'TechOnTheNet';

console.log(totn_string.includes('e'));

3. var totn_string = 'TechOnTheNet';

console.log(totn_string.includes('The'));

indexOf - this method returns the first index at which a given element can be found in the array, or -1 if it is not present.

examples
1. const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// expected output: 1

2. var array = [2, 9, 9];
array.indexOf(2);     // 0
array.indexOf(7);     // -1
array.indexOf(9, 2);  // 2
array.indexOf(2, -1); // -1
array.indexOf(2, -3); // 0

3. const letters = ['a', 'b', 'c']

const index = letters.indexOf('b')

//index is `1`

every - this method tests whether all elements in the array pass the test implemented by the provided function. it returns a boolean value. 

examples
1. const isBelowThreshold = (currentValue) => currentValue < 40;

const array1 = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
// expected output: true

2. function isBigEnough(element, index, array) {
  return element >= 10;
}
[12, 5, 8, 130, 44].every(isBigEnough);   // false
[12, 54, 18, 130, 44].every(isBigEnough); // true

3. [12, 5, 8, 130, 44].every(x => x >= 10);   // false
[12, 54, 18, 130, 44].every(x => x >= 10); // true