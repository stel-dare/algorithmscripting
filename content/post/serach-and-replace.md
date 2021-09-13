+++
author = "Stella Dare"
title = "Search And Replace."
date = "2020-12-23"
description = "Search for a word and replace it. "
tags = [
    "Intermediate",
    "JavaScript",
    "replace",
    
]
level = "2. Intermediate"
series = "Coding Challenges"
aliases = [""]
+++

 You have a sentence or paragraph and you want to replace a word with another word. You want to preserve the case of the first letter as well. For example, you have a sentence `I love Javascript` and you want to replace `Javascript` with `python`. The result would be `I love Python`. The case is preserved.

<!--more-->

---
## Writing The Function
We would write a function that takes a string, the word to be replaced and the word to be replaced with.

`function replaceWord(str, oldWord, newWord)`.

First we check whether the first letter of  `oldWord` is a capital. If its a capital we capitalize the first letter of `newWord` else we convert `newWord` to lowercase.

We then use the `replace()` method to replace `oldWord` with `newWord`.

To know whether a letter is capitalized or not we check the character code of that letter. From the [Ascii Table](http://www.asciitable.com/) capitalized alphabets A-Z are from 64 to 90. 


{{< highlight js >}}
function replaceWord(str, oldWord, newWord) {
  // Check if the first letter of `oldWord` is a capital
  // If a capital, extract first letter of `newWord` capitalize it and add it
  // to the remaining letters.
  // else convert `newWord` to lowercase  
  newWord = oldWord.charCodeAt(0) <=90
            ? newWord.slice(0,1).toUpperCase() + newWord.slice(1) 
            : newWord.toLowerCase();
  
  // Replace `oldWord` with `newWord` and return results.
  return str.replace(oldWord,newWord);
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
replaceWord("Let us go to the store", "store", "mall");
// Output
"Let us go to the mall"

replaceWord("His name is Tom", "Tom", "john");
// Output
"His name is John"

replaceWord("This has a spellngi error", "spellngi", "spelling");
// Output
"This has a spelling error"
{{< /highlight >}}

Happy Coding! Read more about [charCodeAt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt) [replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace) and [Ascii Table](http://www.asciitable.com/).