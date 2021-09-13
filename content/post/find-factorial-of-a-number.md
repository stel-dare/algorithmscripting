+++
author = "Stella Dare"
title = "Find Factorial of A Number"
date = "2020-09-01"
description = "Find the factorial of a number"
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
    "Recursion",
]
level = "1. Basic"
series = "Coding Challenges"
aliases = ["use-recursion-to-factorialize-a-number"]
+++

To find the factorial of a number, we'd have to find the product of all positive number less than or equal to that number. For example, the factorial of `5` is `5*4*3*2*1` which is `120`. One simple way of doing this is to use `recursion`. 
<!--more-->

## Using Recursion
With `recursion` we would keep calling the function on itself till a `condition` is met. Let's write a function that takes a number and returns its factorial.

{{< highlight js >}}
function factorialize(num) {
  // Define variable to store product.
  // We are initializing this variable with 1 because any number multiplied by 1 doesnt change.
  let product=1;
  // This is the condition to stop the recursion when num <=1 because we only want the product
  // of positive numbers.
  if(num<=1) return product;
  //Multiply what's in product by num
  product*=num;
  // Keep calling our factorialize function while decrementing the value of num by 1.
  return factorialize(num-1)*product;
}
{{< /highlight >}}

## Testing the function
{{< highlight js >}}
factorialize(10);
// Output
3628800
{{< /highlight >}}

Recursion can very confusing. It took me a while to grasp it myself. In fact I don't think I fully understand it because I find it difficult explaining it.  I hope this helped.
Happy Coding!