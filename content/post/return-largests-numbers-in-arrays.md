+++
author = "Stella Dare"
title = "Return Largest Numbers In Arrays"
date = "2020-09-05"
description = "Find the largest numbers in  arrays"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["return-the-smallest-number-in-arrays"]
+++

You are to write a function that takes a `two dimensional array` and returns an `array` consisting of the largest  number from each provided sub-array. You would need to use a `loop` to achieve this.
<!--more-->

---
## Writing The Function
There are a lot of loops you can use to write this function. The `for`, `while`, `do while` etc. I love the `forEach` method. The `forEach` method takes a `function` loops through an array and applies that function to every element of that array. In our case its would loop through our `two dimensional array` and find the max of each inner array.

{{< highlight js >}}
function largestInArrays(multiArr){
    // Define array to store our max values
    let largest = [];
    // Loop through array with forEach
    multiArr.forEach((innerArr)=>{
        // Find max of each inner array using the math function
        let max = Math.max(...innerArr);
        // Push max into our storage array
        largest.push(max);
    });
    // Return array of max values when loop is done
    return largest;
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
largestInArrays([[4, 9, 1, 3], [13, 35, 18, 26], [32, 35, 97, 39], [1000000, 1001, 857, 1]]);

// Output
[ 9, 35, 97, 1000000 ]
{{< /highlight >}}
I hope this helped. Read more about the [forEach method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach). Here is also [a list of JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp). Happy Coding!