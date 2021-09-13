+++
author = "Stella Dare"
title = "Wherefore art thou."
date = "2020-12-21"
description = "Return array of object that have matching key value pairs. "
tags = [
    "Intermediate",
    "JavaScript",
    "filter",
    "every"
]
level = "2. Intermediate"
series = "Coding Challenges"
aliases = ["return-an-array-of-object-that-have-matching-key-value-pairs"]
+++

You have an array of objects but you only need the objects that have a specific key value pair. Example you want only objects that have a `firstname` key with a value `hermione`. 

<!--more-->

---
## Writing The Function
We have our array of objects, but we want only the objects that have specific key value pairs. Our array of object would be the first argument. The second argument would be the specific key value pairs we need. eg `{firstname:'Steve',lastname:'Rogers}` or `{carType:'electric'}`.  

First we `filter` through the array of objects. Filter would return the objects that evaluate to true(that is objects that contain the key/value pirs we want). We then use the `every` method inside the filter to check if the object provided by the filter method has the key/value we need. The every method returns true or false to the filter method. The filter method would then return only the objects that evaluated to true.


{{< highlight js >}}
function filterCollection(collection, query) {
    // Let's get all the keys in the query
    let queryKeys = Object.keys(query);

    // Filter the collection array to return only objects which have the properties 
    // in the query object
    return collection.filter((obj)=>{
        // return true for obj in our collection that have the key value pair
        // specified in our query object.
        return queryKeys.every(key => key in obj && obj[key] === query[key]);
    });
}
{{< /highlight >}}

## Testing The Function
{{< highlight js >}}
filterCollection(
    [
        { first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }
    ] ,
    { last: "Capulet" }
 );

// Output
[{ first: "Tybalt", last: "Capulet" }]


filterCollection(
    [
        { "apple": 1, "bat": 2 }, { "apple": 1 }, { "apple": 1, "bat": 2, "cookie": 2 }
    ], 
    { "apple": 1, "cookie": 2 }
);

// Output
[{ "apple": 1, "bat": 2, "cookie": 2 }]
{{< /highlight >}}

Happy Coding! Read more about [filter()](https://www.w3schools.com/jsref/jsref_filter.asp), [every()](https://www.w3schools.com/jsref/jsref_every.asp), [in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in) and other [JavaScript array methods](https://www.w3schools.com/jsref/jsref_obj_array.asp).