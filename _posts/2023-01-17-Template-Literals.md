---
layout: post
title:  "Template Literals"
---

Template literals are a feature in JavaScript that allow you to create strings with placeholders that are replaced with values at runtime. 
They are defined using backticks () instead of single or double quotes, and placeholders are defined using the `${expression}` syntax. 
 
One of the cool uses of template literals is the ability to create dynamic DOM elements, which can be useful when working with frameworks like React or Angular.
The process involves creating a string of HTML using template literals, and then using JavaScript to insert that string into the DOM.

For example, consider the following code:

    let name = "John";
    let element = `<div>Hello, ${name}!</div>`;
    document.body.innerHTML = element;
    
In this example, a template literal is used to create a string that represents a div element with the text "Hello, John!". 
The innerHTML property of the document.body object is then set to this string, which adds the div element to the body of the HTML document.

You can also use template literals to create more complex elements with multiple attributes or children elements. For example:

    let title = "My Title";
    let content = "My Content";
    let element = `<div>
                       <h1>${title}</h1>
                       <p>${content}</p>
                   </div>`;
    document.body.innerHTML = element;
    
This will create a div element with a h1 child element with the title and a p child element with the content.

It's also possible to create new DOM elements using JavaScript's createElement() method, and then use template literals to set their attributes and content. 
For example:

    let title = "My Title";
    let content = "My Content";
    let newDiv = document.createElement("div");
    newDiv.innerHTML = `<h1>${title}</h1><p>${content}</p>`;
    document.body.appendChild(newDiv);
    
In this example, the createElement() method is used to create a new <div> element, and a template literal is used to set the element's content by adding an <h1> and <p> tag with the title and content respectively.
The newDiv element is then appended to the body of the HTML document using the appendChild() method.
This way of creating DOM elements is more efficient and flexible than using innerHTML property as it allows you to add elements at specific place in the tree and also it does not affect the performance by replacing the entire content.
