+++
author = "Stella Dare"
title = "Find and replace html entities in a string"
date = "2021-05-23"
description = "Find characters in a string and replace them with their corresponding HTML entities"


series = "Intermediate Algorithm"
aliases = [""]
+++

Write a function that converts the characters `<,>,&,",'` with their corresponding HTML entities. We
would create a `dictionary or an object` with the characters and their corresponding HTML entities and then use a `replace` method to replace every character with its HTML entity using the dictionary as reference. 
<!--more-->

---
## Writing The Function
We use this regular expression `[&<>"']/g` to find all occurrences of `&<>"'` and replace them with their corresponding entity `dict[match]`.
{{< highlight js >}}
function replaceWithHTMLentity(str) {
let  dict = {
    "&":"&amp;",
    "<":"&lt;",
    ">":"&gt;",
    "\"":"&quot;",
    "'":"&apos;"
  }
  return str.replace(/[&<>"']/g, (match)=>dict[match]);
}


replaceWithHTMLentity("Hamburgers < Pizza < Tacos")
// Output
Hamburgers &lt; Pizza &lt; Tacos

replaceWithHTMLentity("Sixty > twelve")
// Output
Sixty &gt; twelve
{{< /highlight >}}


Happy Coding!

