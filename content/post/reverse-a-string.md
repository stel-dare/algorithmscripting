+++
author = "Stella Dare"
title = "Reverse A String"
date = "2020-08-31"
description = "Reversing a string with JavaScript."
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = "Basic Algorithm"
aliases = ["reverse-an-array"]
+++

To reverse a string, we first `split` the string into an array, `reverse` the array and then `join` the array back into a string.
<!--more-->

---
## Applying The Logic
Let's write a function that takes a string and reverses it.

{{< highlight js >}}
function reverseString(string){
    // Split string into an array
    let stringArray = string.split('');
    // Reverse array
    let reverseArray = stringArray.reverse();
    // Join reversed array back to string
    let reverseString = reverseArray.join('');
    // Return reversed string
    return reverseString;   
}
{{< /highlight >}}

## What if there were no *split*, *join* or *reverse* methods
We would reverse the string with a `loop`. Either `for`,`while` or a `do while` loop.

{{< highlight js >}}
function reverseString(string){
    // Define varriable to store reversed string
    let reverseString = '';
    // We want a for loop that starts at the end of the string and loops to the beginning
    // Our loop counter i=string.length-1 because this will makes us start at the end of the string
    // and move towards the beginning. 
    for (let i=string.length-1; i>=0; i--) {
    //Anytime we loop we add that character to our reverseString variable
    //And since we started at the end we would have a reversed string when the loop has ended    
        reverseString+=string[i];
    }
    //Return reversed string
    return reverseString;
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
reverseString("Greetings from Earth");
// Output
htraE morf sgniteerG
{{< /highlight >}}

Here is list of [JavaScript string methods](https://www.w3schools.com/jsref/jsref_obj_string.asp). 
Happy coding!