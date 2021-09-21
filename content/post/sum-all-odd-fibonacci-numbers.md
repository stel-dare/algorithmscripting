+++
author = "Stella Dare"
title = "Sum all odd fibinacci numbers"
date = "2021-09-21"
description = "Sum of all odd Fibonacci numbers that are less than or equal to num"
tags = [
    "Intermediate",
    "JavaScript",
    
]
level = "2. Intermediate"
series = "Coding Challenges"
aliases = [""]
+++

You are given a positive integer and required to return the sum of all odd Fibonacci numbers that are less than or equal to that number. First find all the numbers in the Fibonacci sequence that are less than the number given. And then return only the odd numbers of that sequence. Finally sum the odd numbers and return the sum as the final result.

<!--more-->

---
## THE FIBOBACCI SEQUENCE
The Fibonacci Sequence is a series of numbers. The first numbers in the Fibonacci sequence are `1 and 1`. The next number is found by adding the last two numbers in the sequence. Hence the next number would be `2`. The first six numbers in the sequence are `1, 1, 2, 3, 5, 8`.

Let's solve the problem in the following steps.

#### 1. Find all numbers in the Fibonacci sequence that are less than or equal to the given number
We know that the first two numbers of the sequence are `[1, 1]` and that the next numbers in the sequence are found by adding the last two numbers.

To achieve this step, our starting sequence is
{{< highlight js >}}
let fibSeq = [1,1]; 
{{< /highlight >}}

The next number would be. 
{{< highlight js >}}
fibSeq.slice(-2).reduce((x,y)=> x+y) 
{{< /highlight >}}

`fibSeq.slice(-2)` returns the last two numbers of our array `fibSeq`. The `reduce` method then takes the last two numbers and applies this `(x,y)=> x+y` which is a function that returns the sum of two numbers. Therefore this `fibSeq.slice(-2).reduce((x,y)=> x+y)` would always give us the sum of the last two numbers in the array `fibSeq` which would be the next number in the Fibonacci sequence. Let's simplify it.
{{< highlight js >}}
let sum = (x,y)=> x+y
fibSeq.slice(-2).reduce(sum) 
{{< /highlight >}}

Let's put it all together.
{{< highlight js >}}
function sumFibs(num) {

let fibSeq = [1,1];
let sum = (a,b) => a+b;

// While the next number in the sequence is less than the number given
while(fibSeq.slice(-2).reduce(sum) <= num){
  // Push it into our fibSeq array
  fibSeq.push(fibSeq.slice(-2).reduce(sum))
}

return fibSeq

}
{{< /highlight >}}

#### 2. Return only the odd numbers in the sequence.
If a number is divisible by 2 with no remainder its an `even` number. If it has a remainder its an `odd` number. We calculate the remainder using the `modulo operator %`. That is `10 / 2` is `5` with no remainder. Therefore `10 % 2 == 0`. Also `15 / 2 ` has a remainder therefore `15 % 2 != 0`. This is how we prove that `15 is an odd number`. Let's apply this concept. 

{{< highlight js >}}
function sumFibs(num) {

let fibSeq = [1,1];
let sum = (a,b) => a+b;

// While the next number in the sequence is less than the number given
while(fibSeq.slice(-2).reduce(sum) <= num){
  // Push it into our fibSeq array
  fibSeq.push(fibSeq.slice(-2).reduce(sum))
}

// Filter array fibSeq and return only the odd numbers
return fibSeq.filter( num => num % 2 != 0)

}
{{< /highlight >}}

#### 3. Return the sum of the odd numbers
Finally let's return the sum of the odd numbers.
{{< highlight js >}}
function sumFibs(num) {

let fibSeq = [1,1];
let sum = (a,b) => a+b;

// While the next number in the sequence is less than the number given
while(fibSeq.slice(-2).reduce(sum) <= num){
  // Push it into our fibSeq array
  fibSeq.push(fibSeq.slice(-2).reduce(sum))
}

// Filter array fibSeq and return only the odd numbers
return fibSeq.filter( num => num % 2 != 0).reduce(sum)

}
{{< /highlight >}}

Happy Coding! Reach out to me and let's discuss a different approach.