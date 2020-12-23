+++
author = "Stella Dare"
title = "Pig Latin."
date = "2020-12-22"
description = "Translate A Word To Pig Latin. "
tags = [
    "Intermediate",
    "JavaScript",
    "replace",
    'regex'
    
]
categories = [
    "Intermediate",
]
series = "Intermediate Algorithm"
aliases = ["translate-string-pig-latin"]
+++

Pig Latin is a way of altering English Words. `way` is added to the end of words that begin with a vowel. For words that begin with consonants, the consonant or consonants(if there's more than one) are moved to the end and `ay` is added to the end. 

<!--more-->

---
## Writing The Function
One simple way to achieve this is to use regular expressions. There are two things we want to match. First we want to match words that start with a vowel `aeiou` and add `way` to the end. We can use this regular expression to achieve that `/(^[aeiou])([\w]*)/`. `(^[aeiou])` - capture any vowel that starts a word. `([\w]*)` - capture any alphabets (if any) following the vowel.  We now use the replace method to add `way` to the end. `str.replace(/(^[aeiou])([\w]*)/,'$1$2way')`. `$1` - first thing we captured which is the vowel, `$2` - second thing we captured which any alphabet following the vowel and finally `way`.

We use the same approach to capture consonants (one or more), move then to the end and add `ay`.
`str.replace(/(^[^aeiou]+)([\w]*)/,'$2$1ay')`.


{{< highlight js >}}
function translatePigLatin(str) {
  // Match vowel at begining and add `way` to end and match consonants move them to the end
  // and add `ay`.  
  return str.replace(/(^[aeiou])([\w]*)/,'$1$2way').replace(/(^[^aeiou]+)([\w]*)/,'$2$1ay');
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
translatePigLatin("california");

// Output
"aliforniacay"


translatePigLatin("schwartz");

// Output
"artzschway"

translatePigLatin("rhythm");

//Output
"rhythmay"
{{< /highlight >}}

Happy Coding! Read more about [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) and [replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace).