+++
author = "Stella Dare"
title = "Remove All Falsy Values "
date = "2020-09-30"
description = "Remove all falsy values from an array"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["filter-truthy-values"]
+++

A function that removes all `falsy` values for example `false`, `null` , `0` , `""` values from an array.

<!--more-->

---
## Writing The Function
A value is `falsy` when it does not evaluate to `true`. Therefore we can loop through the array
and only keep the values that evaluate to true.

{{< highlight js >}}
function bouncer(arr) {
    // An array to store values that evaluate to true
  let truthy =[];
  for(let i=0; i<arr.length; i++){
      // If value elavuates to true push to truthy array
      if(arr[i]){
          truthy.push(arr[i]);
      }
  }
  return truthy;
}
{{< /highlight >}}

## A Method That Does The Job
The JavaScript `filter()` method filters an array by returning all values that pass a test.
{{< highlight js >}}
function bouncer(arr) {
// Return values that evaluate to true
return arr.filter(elem=>elem);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
bouncer([7, "ate", "", false, 9]);
// Output 
[7, "ate", 9]

bouncer([false, null, 0, NaN, undefined, ""]);
// Output 
[]
{{< /highlight >}}

Happy Coding! Read more about the [filter() method](https://www.w3schools.com/jsref/jsref_filter.asp).
