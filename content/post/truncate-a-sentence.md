+++
author = "Stella Dare"
title = "Truncate A Sentence"
date = "2020-09-27"
description = "Truncate a sentence"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["truncate-a-string"]
+++

Let's write a function that truncates a sentence to any maximum number of words. 
<!--more-->

---
## Writing The Function
{{< highlight js >}}
function truncateString(str, num) {
    // Return string if string length is less than or equal to the maximum number
  if(str.length <= num) return str;
  // Slice string and add '...' 
  return str.slice(0,num) + '...';
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
truncateString("A-tisket a-tasket A green and yellow basket", 8);
// Output
"A-tisket..."

truncateString("Peter Piper picked a peck of pickled peppers", 11);
// Output
"Peter Piper..."
{{< /highlight >}}

Happy Coding!