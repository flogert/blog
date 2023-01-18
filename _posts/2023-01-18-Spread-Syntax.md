---
layout: post
title:  "Spread Syntax"
---

The spread syntax is a feature of JavaScript that allows an iterable (such as an array or an object) to be expanded in places where zero or more arguments or elements are expected. It is represented by three dots (...).

For example, in an array literal, the spread syntax can be used to spread the elements of an existing array into a new array:

    let array1 = [1, 2, 3];
    let array2 = [4, 5, 6];
    let array3 = [...array1, ...array2];
    console.log(array3); // [1, 2, 3, 4, 5, 6]

In function calls, the spread syntax can be used to spread the elements of an array as individual arguments:

    let array = [1, 2, 3];
    console.log(Math.max(...array)); // 3

The spread syntax can also be used to create a new object that inherits properties from an existing object.

    let obj1 = {a:1, b:2}
    let obj2 = {...obj1, c:3}
    console.log(obj2) // {a:1, b:2, c:3}

It can also be used to combine multiple object into one

    let obj1 = {a:1, b:2}
    let obj2 = {c:3, d:4}
    let obj3 = {...obj1, ...obj2}
    console.log(obj3) // {a:1, b:2, c:3, d:4}

In summary, the spread syntax can be used to easily and concisely expand the elements of an iterable (such as an array or an object) into a new context, such as an array literal, a function call, or an object literal.
