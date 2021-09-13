+++
author = "Stella Dare"
title = "DNA Pairing"
date = "2021-01-24"
description = "Pairing DNA strands"
tags = [
    "Intermediate",
    "JavaScript",
    "map",
    
]
level = "2. Intermediate"
series = "Coding Challenges"
aliases = [""]
+++

DNA consists of a pair of strands that are tightly held together. The units `A, T, C, G` make up the pair of strands. A always pairs with T and T always pairs with A `[AT,TA]`. C always pairs with G and G always pairs with C `[CG,GC]`. You want a function that pairs a string of single DNA strands.
<!--more-->

---
## Writing The Function
We would first have to define a dictionary for our function to refer to. 
 `let dict={ A:'T', T:'A', C:'G', G:'C'}`.
 We then split the string and pair each character. 

{{< highlight js >}}
function pairDNA(str) {
  // Dictionary for function to refer to  
  let dict={
    A:'T',
    T:'A',
    C:'G',
    G:'C'
  }

  // Split string into an array.
  // For each character return an array of the strand and its pair.
  return str.split('').map(char=>[char,dict[char]]);
}

{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
pairDNA("ATCGA");
// Output
[["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]]

pairDNA("TTGAG");
// Output
[["T","A"],["T","A"],["G","C"],["A","T"],["G","C"]]

pairDNA("CTCTA")
// Output
[["C","G"],["T","A"],["C","G"],["T","A"],["A","T"]]
{{< /highlight >}}

Happy Coding! Read more about [map()](https://www.w3schools.com/jsref/jsref_map.asp).