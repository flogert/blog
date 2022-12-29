---
layout: post
title:  "'This' in JavaScript"
---

In JavaScript, the this keyword refers to the object that is currently executing the code. The value of this can change depending on how the code is called.

Here are some examples of how this can be used in JavaScript:

In a regular function, this refers to the global object (either window in the browser or global in Node.js).
For example:


    function test() {  

    console.log(this);  
  
    }  


    test(); // logs the global object


In an object method, this refers to the object itself.
For example:


    const obj = {  

    prop: 'Hello',  

    greeting: function() {  
  
    console.log(this.prop);  
    
    }  
  
    }  


    obj.greeting(); // logs 'Hello'


In a class method, this refers to the instance of the class.
For example:


    class MyClass {  

    constructor(prop) {  

      this.prop = prop;  

    }  


    greeting() {  

      console.log(this.prop);  

    }  

    }  


    const instance = new MyClass('Hello');  

    instance.greeting(); // logs 'Hello'  



this can also be bound explicitly using the call, apply, or bind methods.
For example:

     function test() {  

    console.log(this.prop);  

     }  


    const obj = { prop: 'Hello' };  


    test.call(obj); // logs 'Hello'  

