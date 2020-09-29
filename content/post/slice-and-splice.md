+++
author = "Stella Dare"
title = "Copy An Array Into Another Array "
date = "2020-09-28"
description = "Copy an array into another array"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["copy-array-into-another-array"]
+++

A function that copies an array into another array at any index.

<!--more-->

---
## Writing The Function
We can use the `slice` and `splice` methods to solve this. The `slice` helps us copy an array and the 
`splice` allows us to insert elements into an array. This function would copy the first array into 
the second array at a given index.
{{< highlight js >}}
function frankenSplice(arr1, arr2, n) {
    // Copy arr2 into newArr because we don't want splice to mutate the original array.
   let newArr = arr2.slice();
   // Use splice to copy arr1 into newArr at the given index
   newArr.splice(n,0,...arr1);
   // Return newArr
   return newArr;
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
frankenSplice([1, 2, 3], [4, 5], 1);
// Output
[4, 1, 2, 3, 5]

frankenSplice(["claw", "tentacle"], ["head", "shoulders", "knees", "toes"], 2);
// Output
["head", "shoulders", "claw", "tentacle", "knees", "toes"]
{{< /highlight >}}

Happy Coding! Read more about the [slice](https://www.w3schools.com/jsref/jsref_slice_array.asp) and [splice](https://www.w3schools.com/jsref/jsref_splice.asp) methods.