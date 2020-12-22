+++
author = "Stella Dare"
title = "Spinal Tap case."
date = "2020-12-21"
description = "Convert a string to spinal case. "
tags = [
    "Intermediate",
    "JavaScript",
    "split",
    "join"
]
categories = [
    "Intermediate",
]
series = "Intermediate Algorithm"
aliases = ["convert-string-to-spinal-case"]
+++

You have a string in mixed casing eg. `thisIsSpinalTap, The_Andy_Griffith_Show, AllThe-small Things` and you want to convert it to spinal case. eg. `all-the-small-things`

<!--more-->

---
## Writing The Function
We have a string that could be in any casing and we have to convert it to spinal case. 
First with `split` the string with a `regular expression` `/\W|_|(?=[A-Z])/`. This splits the string into an array with any of the following as dilimeters `\W` -  non-alphabets, `_` - underscore, `(?=[A-Z])` - positive lookahead (separate by capital case but do not remove capital case). Then we join the array returned with a hyphen `-` and convert to lowercase.


{{< highlight js >}}
function spinalCase(str) {
    // Separate string with split using regular expressions
    // join with hyphen `-` and convert to lowercase.
  return str.split(/\W|_|(?=[A-Z])/).join('-').toLowerCase();
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
spinalCase("This Is Spinal Tap");

// Output
"this-is-spinal-tap"


spinalCase("The_Andy_Griffith_Show");

// Output
"the-andy-griffith-show"

spinalCase("AllThe-small Things")

//Output
"all-the-small-things"
{{< /highlight >}}

Happy Coding! Read more about [split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split), [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) and [join()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join).