# Functional Programming & Node.js Video 

Reading assignment for Class 09

## Questions & Answers

[Functional Programming Concepts](https://github.com/tk-notes/fp-in-javascript-article-source-code)

1. What is functional programming? It is a programming paradigm with a purpose of removing situations of unknown errors by focusing on functions with specific and clear parameters. Trying not to rely on any global variables as inputs.
2. What is a pure function and how do we know if something is a pure function? It returns the same result if given the same arguments and has no side effects.
3. What are the benefits of a pure function? Code is a bit more intuitive to understand. Reliability, and predictability.
4. What is immutability? The condition of not being changeable.
5. What is Referential transparency? An expression that can be replaced with its value without altering the behavior of the application.

---

[NodeJS Tutorial for Beginners # ^ - Modules and Require() *Video*](https://www.youtube.com/watch?v=xHLd36QoS4k)

1. What is a module? A module is a separate file within an application. It can have JSON data, JS code, etc.
2. What does the word 'require' do? Require is a way to import modules.
3. How do we bring another module into the file that we are working in? We use the function `require()` as well as on the module that you want exported `module.exports = functionName`
4. WHat do we have to do to make a module available? Use the `module.exports = module/functionName`

## Functional Programming

### What is it?

> Functional Programming is a programming paradigm - a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data [Wikipedia](https://en.wikipedia.org/wiki/Functional_programming)

### Pure Functions

* **Deterministic:** It returns the same result if given the same arguments.
* **No Side Effects:** It does not cause any observable side effects.

#### Pure vs Impure Functions

**Impure Example:**

This is impure because it uses a global object `PI` that wasn't passed into the function as a parameter. So if `PI` randomly changes without being aware then it cause an unobservable side effect to the result.

* **Reading Files** - If the function reads external files, it's not pure as the file's contents can change.
* **Random Number Generation** - Any function that relies on an *RNG* can never be pure.

```javascript
const PI = 3.14;

function calculateArea(radius) {
     return radius * radius * PI
}

calculateArea(10); //returns 314.0
```

**Pure Example:**

This is pure because the value of `PI` can be changed through the argument either referring to the global object or something different.

```javascript
const PI = 3.14;

function calculateArea(radius, pi) {
     return radius * radius * pi;
}

calculateArea(10, PI); // returns 314.0
```

**Impure `increaseCounter` Example:**

Notice how the global value of `counter` is adjusted.

```javascript
let counter = 1;

function increasedCounter(value) {
counter = value +1;
}

increaseCounter(counter);
console.log(counter); //2
```

**Pure `increaseCounter` Example:** 

Mutability is discouraged, so the global value of `counter` remains the same. Yet function works the same.

```javascript
let counter = 1;

function inscaredCounter(value) {
     return value + 1;
}

increaseCounter(counter); //2
```

### Pure Function Benefits

* Code is easier to test
* Can test pure functions with different contexts:
  * Give parameter `A` -> expect the function to return value `B`
  * Give parameter `C` -> expect the function to return value `D`

```javascript
let list = [1, 2, 3, 4, 5];

function incremenetNumbers(list) {
     return list.map(number => number + 1)
}

incremenetNumbers(list); // [2, 3, 4, 5, 6]
```

### Immutability

>Unchanging over time or unable to be changed.

Simplifies tracking changes and understanding code flow.

**Mutable Example:**

Here `sumOfValues` is being changed, as well as `[i]` within the function.

```javascript
var values = [1, 2, 3, 4, 5];
var sumOfValues = 0;

for (var i = 0; i < values.length; i++) {
	sumOfValues += values[i];
}

console.log(sumOfValues); // 15
```

**Immutable Example:**

Here neither `list` nor `accumulator` end up being changed thanks to the recursive nature of the function.

```javascript
let list = [1, 2, 3, 4, 5];
let accumulator = 0;

function sum(list, accumulator) {
     if (list.length ==0) {
     return accumulator;
     }
	
  return sum(list.slice(1), accumulator + list[0]);
}

sum(list, accumulator); //15
console.log(list); // [1, 2, 3, 4, 5]
console.log(accumulator); //0
```
### Referential Transparency

**Concept:** An expression that can be replaced with its value without altering the behavior of the program.

```javascript
function square(n) {
     return n * n;
}
// square(2) is referentially transparent as it can be replaced with 4
```

### Functions as First-Class Citizens

Functions can be assigned to variables, passed as arguments, or returned from other functions.

```javascript
const double = n => n * 2;
const numbers =[1, 2, 3];
const doubledNumbers = numbers.map(double);
// Functions like 'double' can be used as data
```

### Higher-Order Functions

Functions that operate on other functions, either by taking them as arguments or by returning them.

Common examples: `map`, `filter`, `reduce`.

## Node.js Modules and require()

`require()` is a global function provided by Node.js. It is used to import modules, JSON, and local files.

To use it you'll need to add `const funcitonName =require('fileLocation')` to the separate file that you'd like to use it in.

On the module that contains the actual function you will need to add `module.exports = functionName`. 
