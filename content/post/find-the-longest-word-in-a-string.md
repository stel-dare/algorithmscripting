+++
author = "Stella Dare"
title = "Find The Longest Word In A String"
date = "2020-09-02"
description = "Find The Longest Word In A Sentence."
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = ["Basic Algorithm"]
aliases = ["find-the-shortest-word"]
+++

To find the longest word in a string we first split the sentence into an `array` of `words` and `loop` through the array to find the longest word. 
<!--more-->

## Applying The Logic
Lets write a function that takes a sentence and returns the longest word in that sentence.
{{< highlight js >}}
function longestWord(sentence){
    // Split sentence into an array of words.
    let words = sentence.split(' ');
    // Define variable to store longestWord
    let longestWord ="";
    // Define variable to store longestWord length
    let longestWordLength=0;
    //Loop through the words array
    for(let i=0; i < words.length; i++){
        // Check if a word's length is longer than whats in the longestWordLength variable.
        if(longestWordLength < words[i].length){
            // Replace longestWordLength with the length of the longer word
            longestWordLength = words[i].length;
            // Replace longestWord with the longer word.
            longestWord = words[i];
        }
    }
    // Return the longestWord varriable after the loop is done
    return longestWord;   
}
{{< /highlight >}} 

## Another Method.
We can also find the longest word by using javascript's `reduce` method to reduce our `array` of `words` into the longest word.
{{< highlight js >}}
function longestWord(sentence){
    // Split sentence into an array of words.
    let words = sentence.split(' ');
    // The reduce method is used to evaluate an array into a single value after 
    // looping through the whole array.
    // In this case we use the reduce metods to loop through our array of words
    // and keep checking whether we have the longest word.
    // It would return the longest word when the loop has ended.
  return  words.reduce((longWord,word)=>{
        if(word.length>longWord.length){
            longWord = word;
        }
        return longWord;
    },"");
}
{{< /highlight >}} 

I hope this helped. The [reduce method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce) is explained in more details [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce). Here is also [a list of JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp). Happy Coding!