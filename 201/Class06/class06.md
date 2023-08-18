# Class 6 Reading Assignment

Reading assignment 'Read 06'

## Questions and Answers

### JavaScript

1. How would you describe an object to a non-technical friend you grew up with? If you take your diver's license and notice that it holds separate pieces of information about you like your name, address, height, if you are a donor, etc. Objects in JavaScript are a lot like the diver's license, where it holds various types of information. It goes a step further in being able to provide multiple types of functions, which are called methods.
2. What are some advantages to creating object literals? It creates an entirely more dynamic way of interacting with different types of data. Objects are to make functions act in an even more dynamic way. They can hold a large of amount of data that is structured in a way holds similar data. Being in an object you can interact with the different properties.
3. How do objects differ from arrays? Arrays are a linear way of holding multiple types of data. Objects can hold methods(functions) within itself.
4. Give an example for when you would need to use bracket notation to access an object's property instead of dot notation. If the Object property is within a variable, and you need to find the Object properties value.
5. Evaluate the code below. What does the term `this` refer to, and what is the advantage to using `this`? `this` is referring to current object. The advantage of using `this` is the ability to refer to the properties and methods of the current object regardless of where the object was created.

  ``` JS
      const dog = {
      name: 'Spot',
      age: 2,
      color: 'white with black spots',
      humanAge: function (){
        console.log(`${this.name} is ${this.age*7} in human years`);
      }
    }
  ```

-----------------------------------------------------------

### Introduction To The DOM

1. What is the DOM? Stands for Document Object Model. It is a coded copy of the entire HTML file, allowing things to edit on/off, and create more of a dynamic experience for the user. This can include things like a mouse hovering over a button or link.

2. Briefly describe the relationship between the DOM and JavaScript. Overall, the DOM represents the structure of the HTML document as a tree of nodes, where each node corresponds to an element, attribute, or text within the HTML. The relationship with JavaScript is that it acts as the bridge for JavaScript to make the HTML file dynamic.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[JavaScript Object Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics) \| [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

## JavaScript Objects

> An object is a collection of related data and/or functionality.

Objects can hold multiple various and properties/methods (functions when inside objects).

**Example:**

``` JS

const person = {
  name: ["Bob", "Smith"],
  age: 32,
  bio() {
    console.log(`${this.name[0]} ${this.name[1]} is ${this.age} years old.`);
  },
  introduceSelf() {
    console.log(`Hi! I'm ${this.name[0]}.`);
  },
};

```

* `person` - is the object
* `name`, `age` - are object properties that hole any type of value
* `bio()`, `introduceSelf()` - are object methods that act as functions

### Dot Notation

``` JS
person.age;
person.bio();
```

Similar to calling a function you need to use the object name then with the dot nation `.` you can access the properties or methods within the object.

### Bracket Notation

``` JS
person["age"];
person["bio"]();
```

Not the standard notation used, but when the property name is held in a variable you have to use bracket notation to access the value.

``` JS
  const person = {
  name: ["Bob", "Smith"],
  age: 32,
};

function logProperty(propertyName) {
  console.log(person[propertyName]);
}

logProperty("name");
// ["Bob", "Smith"]
logProperty("age");
// 32
```

If you were to type in the `console.log(person.propertyName)` you would simply get undefined as that would think you are console logging a property within the `person` object named `propertyName` which does **not** exist within the object, thus returning `undefined`.

### What is "this"?

``` JS
  introduceSelf() {
  console.log(`Hi! I'm ${this.name[0]}.`);
}
```

`this` - refers to the current object. It offers efficiency when it comes to creating a function with an object nested inside.

## Introduction to the DOM

`DOM` - Document Object Model, a coded copy of the entire HTML file, allowing things to edit on/off, and create more of a dynamic experience for the user. This can include things like a mouse hovering over a button or link.

Overall, the DOM represents the structure of the HTML document as a tree of nodes, where each node corresponds to an element, attribute, or text within the HTML.

**List of commands:**

* `document.querySelector("selector");`
* `document.appendChild("childNode");`
* `document.getElementById("elementId");`
* `document.createElement("tagName");`

