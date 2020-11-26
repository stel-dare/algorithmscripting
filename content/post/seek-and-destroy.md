+++
author = "Stella Dare"
title = "Seek and Destroy."
date = "2020-11-26"
description = "Seek and remove elements in an array."
tags = [
    "Intermediate",
    "JavaScript",
    "filter",
    "args",
    "includes"
]
categories = [
    "Intermediate",
]
series = "Intermediate Algorithm"
aliases = ["remove-elements-in-an-arry-that-are-in-a-second-array"]
+++

You are provided with an initial array followed by one or more arguments. Remove all elemets from the initial array that are of the same value as the remaining arguments.

<!--more-->

---
## Writing The Function
We are given an array of elements as the first argument and 1, 2 or more other arguments. We use the 
`args` object to store the remaining arguments not matter how many they are. We then essentially end up
with two arrays, the `initial array` and the `args array`. We now use the `filter method` to return elements that are in the initial array but not in the args array.
{{< highlight js >}}
function destroyer(arr,...args) {
  // The arrgs object will give us an array of all 
  // the remaining arguments.
  // Use filter method to return elements that 
  // are not found in the args array.
  return arr.filter((elem) => 
  // Return only elements that are not found
  // in the args array.
  !args.includes(elem));
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
destroyer([1, 2, 3, 1, 2, 3], 2, 3);

// Output
[1, 1]

destroyer(["tree", "hamburger", 53], "tree", 53);

// Output
["hamburger"]
{{< /highlight >}}

Happy Coding! Read more about [args](https://www.w3schools.com/js/js_es6.asp#mark_rest), [filter()](https://www.w3schools.com/jsref/jsref_filter.asp) ,[includes](https://www.w3schools.com/jsref/jsref_includes_array.asp) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).