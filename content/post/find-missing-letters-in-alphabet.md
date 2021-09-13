+++
author = "Stella Dare"
title = "Find missing letters in the alphabet"
date = "2021-04-24"
description = "First the first missing letter in a string of alphabets"

tags = [
    "Intermediate",
    "JavaScript",    
]

series = "Coding Challenges"
level = "2. Intermediate"
aliases = [""]
+++

Write a function that when given a string of alphabets `abce`, it returns the first missing letter which would be `d` in this case. We would convert the string into `ASCII  codes` loop through it and check if the code of a letter plus one is equal to the next code. If its not, a letter is missing and that missing letter would be the current code plus one. Let's get into it. 
<!--more-->

---
## Writing The Function
First we split the string into an array and map over it to convert each string into its `ASCII` code.
So a string `abcde` would become `[ 97, 98, 99, 101 ]`. Since the string is in an alphabetical order the difference between one code and the next should be `1`.

We then `loop` through this array and check if the difference between one code and the next is `1`. 
if the difference is not `1` then there's a missing letter between those two codes.

The missing letter therefore would be the current code plus one converted back to a letter.

{{< highlight js >}}
function findMissingLetter(str) {
  
  let strArray = str.split('').map(e=>e.charCodeAt(0));

  for(let i=0; i<strArray.length; i++){
    
    if(i != strArray.length - 1 && strArray[i]+1 != strArray[i+1] ){
      return String.fromCharCode(strArray[i]+1);
    }
  }

}

findMissingLetter("abce");
// Output
d

findMissingLetter("abcdefghjklmno");
// Output
i

{{< /highlight >}}


Happy Coding! Feel free to reach out to me to discuss a different approach.

