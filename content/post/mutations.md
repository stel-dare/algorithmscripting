+++
author = "Stella Dare"
title = "Check If String Contains All Letters Of Another String"
date = "2020-09-30"
description = "Check If String Contains All Letters Of Another String"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["sort-an-array"]
+++

A function that checks if all letters of one string are present in the other.

<!--more-->

---
## Writing The Function
{{< highlight js >}}
function mutation(arr) {
  // Split the second word into an array
  return arr[1].split('')
  // Use JavaScript every() method to return true when every letter is found
  .every(letter=>
  // Use regular expresion to test for the letter case insensitive
  RegExp(letter,'i').test(arr[0]));
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
mutation(["hello", "hey"]);
// Output
false

mutation(["Alien", "line"]);
// Output
true
{{< /highlight >}}

Happy Coding! Read more about [every()](https://www.w3schools.com/jsref/jsref_every.asp), [regular expressions](https://www.w3schools.com/jsref/jsref_obj_regexp.asp) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).