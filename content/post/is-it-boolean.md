+++
author = "Stella Dare"
title = "Check If Boolean Primitive"
date = "2020-09-28"
description = "Check if a value is a boolean primitive"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["is-boolean"]
+++

A function that checks if a value is a true boolean that is `true` or `false`.
<!--more-->

---
## Writing The Function
{{< highlight js >}}
function booWho(bool) {
  // Compare type of value and return true or false
  return typeof bool === 'boolean';
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
booWho(true)
// Output
true

booWho(false)
// Output
true

booWho([1, 2, 3])
// Output
false
{{< /highlight >}}

Happy Coding!

