+++
author = "Stella Dare"
title = "Sum All Numbers In A Range"
date = "2020-11-21"
description = "Split All Numbers In A Range"
tags = [
    "Intermediate",
    "Algorithm",
    "JavaScript",
    "while loop",
    "loop",
    "range"
]
level = "2. Intermediate"
series = "Coding Challenges"
aliases = ["add-numbers-in-a-range"]
+++

Write a function that takes an array of two numbers and returns the sum of those
two numbers and all the numbers between them.

<!--more-->

---
## Writing The Function
We first have to find the `maximun` and `minimum` of the values given us. We create a new `array` and use
a `loop` (could be a for loop or a while loop) to push the numbers from the minimum to the maximum
into that `array`.

We would now have an array of the numbers from the minimum to the maximum. We finally use JavaScript's `reduce` method to sum all the numbers in the array and then `return` the results.
{{< highlight js >}}
function sumAll(arr) {
  // Lets find the maxinum and minimum values in our  array
  let max = Math.max(...arr);
  let min = Math.min(...arr);
  // Initialize an empty array that would store our range
  let range = [];
  // A while loop to push the range of numbers from the
  //minimun to the maximun into our array
  while(min<=max){
    range.push(min);
    min++;
  }
  // Use the reduce method to sum the numbers in our
  //array and return the result.
  return range.reduce((total,num)=>total+num);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
sumAll([1, 4]);
// Output
10

sumAll([10, 5]);
// Output
45
{{< /highlight >}}

Happy Coding! Read more about [loops](https://www.w3schools.com/js/js_loop_for.asp), [reduce()](https://www.w3schools.com/jsref/jsref_reduce.asp) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).