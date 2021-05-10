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
