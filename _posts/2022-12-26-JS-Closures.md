---
layout: post
title:  "JavaScript Closures"
---

JavaScript closures are a fundamental concept in the JavaScript programming language that enables developers to write more powerful and efficient code. In this article, we'll explore what closures are, how they work, and how to use them in your own programs.

What are Closures?

A closure is a function that remembers and has access to variables and arguments from its parent scope, even after the parent function has finished executing. This allows the closure to retain its state and continue to reference and manipulate variables from the parent scope, even after the parent function has been called.

To understand closures, it's important to first understand the concept of lexical scoping in JavaScript. Lexical scoping refers to the way in which the JavaScript interpreter determines the scope of a variable by looking at its position in the source code. In JavaScript, each time a function is defined, it creates a new scope. This means that variables defined within a function are only accessible within that function, and not in the global scope or any other nested scopes.

Let's look at an example to illustrate how closures work:\n


<code>
function greet(name) {\n
  let greeting = "Hello, ";\n
  return function() {\n
    console.log(greeting + name);\n
   }\n
}\n
  
</code>
<code>
let sayHello = greet("John");<br>\n
sayHello(); // Outputs "Hello, John"<br>\n
</code>\n

In this example, we have a function called greet that takes in a name and returns a function that logs a greeting to the console. We then create a variable called sayHello and assign it to the result of calling the greet function with the argument "John".

When we call the sayHello function, it logs the greeting "Hello, John" to the console. But how is it able to remember the value of name and the value of greeting even after the greet function has finished executing?

This is because the inner function that is returned from the greet function has a closure over the variables from the parent scope. This means that the inner function has access to the variables defined in the parent scope, even after the parent function has completed execution.

Why Use Closures?

Closures can be very useful in a number of different situations. One common use case is to create private variables within a function. Because the inner function has a closure over the variables in the parent scope, it can access and manipulate these variables, even though they are not directly accessible from the global scope.

Here's an example of using a closure to create a private variable:\n

<code>
function counter() {\n
  let count = 0;\n
  return function() {\n
    count++;\n
    console.log(count);\n
  }\n
}\n
</code>

<code>\n
let incrementCounter = counter();\n
incrementCounter(); // Outputs 1\n
incrementCounter(); // Outputs 2\n
incrementCounter(); // Outputs 3\n
</code>

In this example, we have a function called counter that defines a private variable called count. We then return an inner function that increments the value of count and logs it to the console.

Because the inner function has a closure over the count variable, it can access and modify it even after the counter function has finished executing. This allows us to create a simple counter that can be incremented multiple times without directly accessing the count variable from the global scope.

Another use case for closures is to enable function factories, which are functions that create and return other functions. 
