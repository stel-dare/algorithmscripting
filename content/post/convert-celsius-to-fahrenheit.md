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
## Applying the formula
Let's write a function that takes a temeperation in Celsius and converts it to Fahrenheit.

{{< highlight js >}}
function convertToFahrenheit(celsius){
    let fahrenheit = (celsius * 9/5)+32;
    return fahrenheit;
}
{{< /highlight >}}
