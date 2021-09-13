+++
author = "Stella Dare"
title = "Split An Array Into Groups Of A Given Size"
date = "2020-09-30"
description = "Split An Array Into Groups Of A Given Size"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["split-array-into-groups"]
+++

A function that splits an array into groups of smaller arrays according to a given size.

<!--more-->

---
## Writing The Function
{{< highlight js >}}
function chunkArrayInGroups(arr, size) {
    // An array to store groups of arrays 
  let chunk=[];
    // Loop through array incrementing by the given size to get the positions of the groups
  for(let i=0; i<arr.length; i+=size){
    // Extract group using slice() and push into chunk
    chunk.push(arr.slice(i,i+size));
  }
  // return groups of array
  return chunk;
  
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
chunkArrayInGroups(["a", "b", "c", "d"], 2);
// Output
[["a", "b"], ["c", "d"]]

chunkArrayInGroups([0, 1, 2, 3, 4, 5, 6], 3);
// Output
[[0, 1, 2], [3, 4, 5], [6]]
{{< /highlight >}}

Happy Coding! Read more about [slice()](https://www.w3schools.com/jsref/jsref_slice_array.asp) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).