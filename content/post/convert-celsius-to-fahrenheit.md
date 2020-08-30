+++
author = "Stella Dare"
title = "Convert Celsius to Fahrenheit"
date = "2020-08-30"
description = "Converting from celsius to fahrenheit with JavaScript."
tags = [
    "Basic",
    "Algorithm",
    "JavaScript",
]
categories = [
    "Basic",
]
series = ["Basic Algorithm"]
aliases = ["convert-fahrenheit-to-celsius"]
+++

The formula for converting from Celsius to Fahrenheit is the temperarue in Celsius, `C` , times `9/5` plus `32`. Thus `F=(C*9/5)+32`.
<!--more-->

---
## Applying The Formula
Let's write a function that takes a temeperature in Celsius and converts it to Fahrenheit.

{{< highlight js >}}
function convertToFahrenheit(celsius){
    let fahrenheit = (celsius * 9/5)+32;
    return fahrenheit;
}
{{< /highlight >}}

## The Reverse - Fahrenheit to Celsius
When you want to convert from Fahrenheit to Celsius you make `C` the subject of the formula `F=(C*9/5)+32`.
Thus `C = (F-32)*5/9`.

{{< highlight js >}}
function convertToCelsius(fahrenheit){
    let celsius = (fahrenheit - 32) * 5/9;
    return celsius;
}
{{< /highlight >}}

Happy coding!