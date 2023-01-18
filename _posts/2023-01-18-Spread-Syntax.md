---
layout: post
title:  "Spread Syntax"
---

The spread syntax (also known as the "spread operator") is a feature of JavaScript that allows you to expand an iterable (such as an array or a string) into individual elements.
It is represented by three dots (...) and can be used in a number of different contexts.
One common use of the spread syntax is to spread the elements of an array into multiple variables.
For example, the following code uses the spread syntax to assign the first and second elements of an array to separate variables:

    let numbers = [1, 2, 3];
    let [a, b, c] = numbers;
    console.log(a);  // 1
    console.log(b);  // 2
    console.log(c);  // 3
    
Another use of the spread syntax is to concatenate arrays. For example, the following code uses the spread syntax to concatenate two arrays into a new one:

    let array1 = [1, 2, 3];
    let array2 = [4, 5, 6];
    let array3 = [...array1, ...array2];
    console.log(array3);  // [1, 2, 3, 4, 5, 6]
    
You can also use the spread syntax to copy an array.

    let array1 = [1, 2, 3];
    let array2 = [...array1];
    console.log(array2);  // [1, 2, 3]

In function calls, the spread operator can be used to pass an array of arguments as individual arguments to a function.

    let numbers = [1, 2, 3];
    console.log(Math.max(...numbers));  // 3

The spread syntax also works with objects, this is called the object rest operator, it works similar to the spread operator in arrays,
but instead of spreading the elements of an array, it spreads the properties of an object.


    let obj = {a: 1, b: 2, c: 3};
    let {a, ...rest} = obj;
    console.log(a);  // 1
    console.log(rest); // { b: 2, c: 3 }

It is important to note that the spread operator creates a shallow copy of an array or object, meaning that if the original array or object contains references to other objects,
the spread copy will contain references to the same objects, so any changes made to those objects will be reflected in both the original and the spread copy.
