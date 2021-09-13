+++
author = "Stella Dare"
title = "Capitalize Each Word In A Sentence"
date = "2020-09-28"
description = "Capitalize each word in a sentence"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["capitalize-sentence"]
+++

Writing a function that capitalizes each word in a sentence.
<!--more-->

---
## Writing The Function
{{< highlight js >}}
function titleCase(str) {
  // Split the sentence into an array of words
  let words = str.split(' ');
  // Loop through array of words and capitalize each word
  for(let i=0; i<words.length; i++){
      // Capitalize first letter of word and lowercase rest of word and concatenate
      words[i] = words[i].slice(0,1).toUpperCase() + words[i].slice(1).toLowerCase();
  }
  // Join words together with space and return
  return words.join(' ');

}
{{< /highlight >}}

## An alternative
We can use any of JavaScript's array methods to loop through the array of methods. Example the
`map` array method.
{{< highlight js >}}
function titleCase(str) {
  // Split the sentence into an array of words
  let words = str.split(' ');
  // Capitalize first letter of word and lowercase rest of word and concatenate
 return  words.map((word)=>word.slice(0,1).toUpperCase() + word.slice(1).toLowerCase())
 // Join words together with space 
 .join(' '); 

}
{{< /highlight >}}


## Testing The Function
{{< highlight js >}}
titleCase("I'm a little tea pot")
// Output
"I'm A Little Tea Pot"

titleCase("sHoRt AnD sToUt")
// Output
"Short And Stout"
{{< /highlight >}}