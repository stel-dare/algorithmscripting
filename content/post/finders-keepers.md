+++
author = "Stella Dare"
title = "Return First Element That Passes Test "
date = "2020-09-28"
description = "Return first element that passes a test"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["find-first-element"]
+++

Write a function that takes an `array` and a `test` as arguments and returns the first element that 
passes the test.

<!--more-->

---
## Writing The Function
{{< highlight js >}}
function findElement(arr, func) {
  // We would store the element that passes the test in this variable
  let elem;
  // Loop through the array and check for any element that passes the test
  for(let i=0; i<arr.length; i++){
    // If an element passes the test we store the element and break from the loop
    if(func(arr[i])) {
      elem=arr[i];
      break;
    } 
  }
  // If elem contains a value return it else return undefined 
  return elem? elem: undefined ;
}
{{< /highlight >}}

## A Simpler Method
JavaScript's `find()` method which loops through and array and returns the first element
that passes a test and `undefined` when no element passes the test.
{{< highlight js >}}
function findElement(arr, func) {
return arr.find(func);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
findElement([1, 3, 5, 8, 9, 10], function(num) { return num % 2 === 0; });
// Output
8

findElement([1, 3, 5, 9], function(num) { return num % 2 === 0; });
// Output
undefined

{{< /highlight >}}

Happy Coding! Read more about the [find method](https://www.w3schools.com/jsref/jsref_find.asp). 

