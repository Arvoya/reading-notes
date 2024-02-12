[[102/README|Module 102]]
# JavaScript

Reading assignment 'Read06'

## Questions & Answers

1. What are variables in JavaScript? can be called by anything but are essentially storage containers that contain a datatype.
2. What does it mean to `declare` a variable? An example of delcaring would be to simply write the command to declare a variable. Such as: `let` or `const`
3. What is an "assignment" operator, and what does it do? these are the many ways you can give a variable a datatype/value. Example: `let x = 3`
4. What is information recieved from the user called? I believe it is called input.

## Notes

Here are the notes I've taken while reading the following blogs:

[JavaScript Intro Paragraph](https://developer.mozilla.org/en-US/docs/Web/JavaScript) \| [Introduction to JavaScript](https://code-maven.com/introduction-to-javascript) \| [JavaScript input with prompt and confrim](https://code-maven.com/javascript-input-with-prompt-and-confirm)

## JavaScript Intro Paragraph

**JavaScript** - (JS) is a programming or scripting language. When used with HTML & CSS, it allows the user to interact with the webpage and have the webpage interact back. Creating a form of unspoken conversation between the user and the website or application.

## Introduction to JavaScript

Traditionally JS was used inside web browsers like Firefox, Chrome, Safari, etc.

### 3 Parts referred to as "JavaScript"

1. The language itself.
2. The DOM API - Currenlty have no idea what this really means.
3. Server API - Also don't really know what this means.

### Embed or Include

You can embed the JavaScript directly inside the HTML file, or put in a line in the HTML file that includes the external JavaScript file. 

To embed the JS directly you need to use the following HTML element: `<script>`

##### Example

``` HTML
<!DOCTYPE html>
<html>
    <head>
        <script>
            console.log("Hello World!")
        </script> 
    </head>
    <body>
    </body>
</html>
```

To use an external JS file, remember to put in the correct element that includes the external JS file.

#### Example

``` HTML
<!DOCTYPE html>
<html>
    <head>
        <script src="[name of js file]"></script>
    </head>
    <body>
    </body>
</html>
```

``` js
console.log("Hellow World!")
```

### Input & Output

A few ways JS can take inputs from a user and output to the website. 

#### Input

` let name = prompt("What is your name?", "");`

#### Output

`document.write("Hello ", name)`