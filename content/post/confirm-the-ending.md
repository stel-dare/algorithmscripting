+++
author = "Stella Dare"
title = "Confirm The Ending Of A String"
date = "2020-09-27"
description = "Confirm the ending of a string."
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["check-the ending-of-a-string"]
+++

We are writing a function that checks if a string ends with a target string.
<!--more-->

---
## Writing The Function
First of we would have to find the `length` of the target string and use it to `slice` the main string from the ending. We then check if the target string and the sliced string are equal.

{{< highlight js >}}
function confirmEnding(str, target) {
    //Find the length of the target string
  let targetLength = target.length;
    // Extract the ending of the main string using targetLength
  let sliceEnding = str.slice(-targetLength);
  // Compare if target string is equal to the main string ending
  return target === sliceEnding;
}
{{< /highlight >}}

## A Simpler Method
We can use the javascript `endsWith()` method. It checks if a given string ends with a target string and
returns `true` or `false`.

{{< highlight js >}}
function confirmEnding(str, target) {
return str.endsWith(target);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
confirmEnding("Open sesame", "same");
// Output
true

confirmEnding("If you want to save our world, you must hurry. We dont know how much longer we can withstand the nothing", "mountain")
// Output
false
{{< /highlight >}}

Happy Coding! Read more about [slice](https://www.w3schools.com/jsref/jsref_slice_array.asp) and [endswith()](https://www.w3schools.com/jsref/jsref_endswith.asp).