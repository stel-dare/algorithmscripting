+++
author = "Stella Dare"
title = "Repeat The String Any Number of Times"
date = "2020-09-27"
description = "Repeat a string any number of times"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["repeat-the-word"]
+++

We are writing a function that repeats a word or sentence any number of times.
<!--more-->

---
## Writing The Function
The function takes a `string` and a `number` and repeats the string that number of times. The function should return an empty string when the number is not positive.  We can use `recursion` or a `loop`.

### Using A For Loop

{{< highlight js >}}
function repeatStringNumTimes(str, num) {
    // Return empty string when num is not positive.
    if(num<1) return '';
    // Variable to store repeated string
    let repeatStr = '';
    // Loop  num times

    for(let i=0; i<num; i++){
        // Add str to repeatStr every loop
        repeatStr+=str;
    }
    // Return repeated string
    return repeatStr;
}
{{< /highlight >}}

### Using Recursion
{{< highlight js >}}
function repeatStringNumTimes(str, num) {
    // Return empty string when num is not positive.
  if(num<1) return '';
    // Keep calling repeatStringNumTimes till num is less than 1
  return str + repeatStringNumTimes(str,num-1);
}
{{< /highlight >}}

### A Much Simpler Way
We can also achieve this using JavaScript's `repeat()` method. 
{{< highlight js >}}
function repeatStringNumTimes(str, num) {
    // Return empty string when num is not positive.
  if(num<1) return '';
  return str.repeat(num);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
repeatStringNumTimes("*", 3);
// Output
"***"
repeatStringNumTimes("abc", 3);
// Output
"abcabcabc"
{{< /highlight >}}


Happy Coding! Read more after the [repeat](https://www.w3schools.com/jsref/jsref_repeat.asp) method.
