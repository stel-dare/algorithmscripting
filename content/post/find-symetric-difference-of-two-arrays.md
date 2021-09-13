+++
author = "Stella Dare"
title = "Find The Difference Between Two Arrays."
date = "2020-11-22"
description = "Find The Difference Between Two Arrays."
tags = [
    "Intermediate",
    "Algorithm",
    "JavaScript",
    "filter",
    "cancat"
]
level = "2. Intermediate"
series = "Coding Challenges"
aliases = ["find-symetric-difference-between-two-arrays"]
+++

Compare two arrays and return a new array with any items only found in one of the two given arrays,
but not both.

<!--more-->

---
## Writing The Function
We first `concat` the two `arrays` in one new  array. We can then use the `filter` method on our new array to filter out the elements that are in one array but not the other and return the results.
{{< highlight js >}}
function diffArray(arr1, arr2) {
  // Concat the given arrays into one array
  let newArr = arr1.concat(arr2);
  // Use filter method on new array to only
  // return elements that pass our condition
  return newArr.filter((elem)=>
  // Our Condition: Check if the current element is not     
  //included in both given arrays
  !(arr1.includes(elem)&&arr2.includes(elem))
  
  );
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
diffArray(
  ["diorite", "andesite", "grass", "dirt", "pink wool",  "dead shrub"],
  ["diorite", "andesite", "grass", "dirt", "dead shrub"]
);

// Output
["pink wool"]

diffArray(
  [1, "calf", 3, "piglet"],
  [1, "calf", 3, 4]
);

// Output
["piglet", 4]
{{< /highlight >}}

Happy Coding! Read more about [concat()](https://www.w3schools.com/jsref/jsref_concat_array.asp), [filter()](https://www.w3schools.com/jsref/jsref_filter.asp) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).