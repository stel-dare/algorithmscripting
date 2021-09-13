+++
author = "Stella Dare"
title = "Find Lowest Index Of Inserted Value "
date = "2020-09-30"
description = "Find the index of an inserted value"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["sort-an-array"]
+++

A function that return the lowest index of a value inserted in an array.

<!--more-->

---
## Writing The Function
{{< highlight js >}}
function getIndexToIns(arr, num) {
  // Add value to array
  return arr.concat(num)
  // Sort array
  .sort((a,b)=>a-b)
  // Find the index of the inserted value
  .indexOf(num);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
getIndexToIns([10, 20, 30, 40, 50], 35);
// Output
3

getIndexToIns([5, 3, 20, 3], 5)
// Output
2
{{< /highlight >}}

Happy Coding! Read more about [concat()](https://www.w3schools.com/jsref/jsref_concat_array.asp) , [sort()](https://www.w3schools.com/jsref/jsref_sort.asp), [indexOf()](https://www.w3schools.com/jsref/jsref_indexof_array.asp) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).
