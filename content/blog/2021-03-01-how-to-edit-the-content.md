---
createdAt: 2022-01-11T19:59:19.490Z
title: What is a spread operator?
description: The spread operator in JavaScript is a useful syntax for adding
  elements to an array, combining arrays into one larger one, spreading an array
  inside the arguments of a function, and more.
---
The spread operator in JavaScript is a useful syntax for adding elements to an array, combining arrays into one larger one, spreading an array inside the arguments of a function, and more.

```js{1,4}\[posts.vue]
// Concatenating arrays and objects
let arr1 = [1,2,3]; 
let arr2 = [4,5]; 
let newArray = [...arr1,...arr2]; 
console.log(newArray);
// Output: [ 1, 2, 3, 4, 5 ] 

// Copying array elements
let arr = ["a","b","c"]; 
let newArray = [...arr]; 
console.log(newArray);
// Output: ["a", "b", "c"]

// Expanding arrays
let arr = ["a","b"]; 
let newArray = [...arr,"c","d"]; 
console.log(newArray);
// Output: ["a", "b", "c", "d"]

// Merging objects
const userBasic = { 
	name: "Jen", 
	age: 22,
}; 
const userMoreInfo = { 
	country: "Argentina", 
	city: "Córdoba", 
}; 
const user = {... userBasic, ... userMoreInfo};
// Output: {  name: "Jen",  age: 22, country: "Argentina", city: "Córdoba"
```