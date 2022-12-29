---
layout: post
title:  "'This' In JavaScript"
---

In JavaScript, the this keyword refers to the object that is currently executing the code. The value of this can change depending on how the code is called.

Here are some examples of how this can be used in JavaScript:

In a regular function, this refers to the global object (either window in the browser or global in Node.js).
For example:

<code>
function test() {\n
  console.log(this);\n
}\n

test(); // logs the global object\n
</code>

In an object method, this refers to the object itself.
For example:

<code>
const obj = {\n
  prop: 'Hello',\n
  greeting: function() {\n
    console.log(this.prop);\n
  }\n
}\n
  
obj.greeting(); // logs 'Hello'
</code>

In a class method, this refers to the instance of the class.
For example:

<code>
class MyClass {\n
  constructor(prop) {\n
    this.prop = prop;\n
  }\n

  greeting() {\n
    console.log(this.prop);\n
  }\n
}\n

const instance = new MyClass('Hello');\n
instance.greeting(); // logs 'Hello'\n
</code>

this can also be bound explicitly using the call, apply, or bind methods.
For example:

<code>
function test() {\n
  console.log(this.prop);\n
}\n

const obj = { prop: 'Hello' };\n

test.call(obj); // logs 'Hello'\n
  
</code>
