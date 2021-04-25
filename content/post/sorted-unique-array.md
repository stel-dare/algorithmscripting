+++
author = "Stella Dare"
title = "Return a sorted unique array given multiple arrays"
date = "2021-04-24"
description = "Return a sorted unique array given two or more arrays as input"


series = "Intermediate Algorithm"
aliases = [""]
+++
You are given two or more array and you're required to return a single array of unique values in the original order in which they appeared in the given arrays. For example given `[1, 3, 2], [5, 2, 1, 4], [2, 1]` return `[1, 3, 2, 5, 4]`. We would first flatten the multiple arrays into a single array and then filter out the duplicates by checking if the index of the current element is equal to the first occurrence of that element. If it is not equal then its a duplicate and filtered out.

<!--more-->

---
## Writing The Function
First we capture the multiple arguments using the spread operator `...`. For example `function uniqueSet(...arr)` and then flatten the array by concatenating them together with the spread operator as well. `let arrFlat =  [].concat(...arr);` . Finally we filter out the duplicates by checking if the index of the current element is equal to the first occurrence of that element. `arrFlat.filter((elem,i)=>arrFlat.indexOf(elem) == i)`

{{< highlight js >}}
function uniqueSet(...arr) {
  let arrFlat =  [].concat(...arr);
  return arrFlat.filter((elem,i)=>arrFlat.indexOf(elem) == i)
}

uniqueSet([1, 3, 2], [5, 2, 1, 4], [2, 1])
// Output
[1, 3, 2, 5, 4]

uniqueSet([1, 2, 3], [5, 2, 1, 4], [2, 1], [6, 7, 8])
// Output
[1, 2, 3, 5, 4, 6, 7, 8]
{{< /highlight >}}


Happy Coding! Feel free to reach out to me to discuss a different approach.

