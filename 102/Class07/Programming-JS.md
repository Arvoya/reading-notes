[[102/README|Module 102]]
# Programming JS

Reading assignmnet 'Read07'

## Questions & Answers

1. What is `control flow`? Control flow is the order in which the computer executes commands.
2. What is a JavaScript `function`? A function is a block of code that is written in a specific way to perform a specific task or (function).
3. What does it mean to `invoke` or `call` a function? Invoke is to create the function by typing it out, and calling a function is when you use it a later point within your script.
4. What are the parentheses `()` for when you define a function? The parentheses are to put in parameters or arguments which can act as values to apply within the function. Or a variables within the function.

## Notes

Here are the notes I've taken while reading the following blogs:

[MDN Control Flow](https://developer.mozilla.org/en-US/docs/Glossary/Control_flow) \| [Functions](https://www.w3schools.com/js/js_functions.asp) \| [Operators](https://www.w3schools.com/js/js_operators.asp) \| [Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) \| [More Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

## Control flow

> The control flow is the order in which the computer executes statements in a script.

> Control flow means that when you read a script, you must not only read from start to finish but also look at program structure and how it affects order of execution.

## Functions

A function is a block of code designed to perform a specific task.

### Syntax

Function is defined with the `function` keyword, followed by a **name**, followed by parentheses `()`.

Function names can contain letters, digits, underscores, and dollar signs.

Parenthenses may include multiple paramater names sparated by commas.

Code that is to be executed by the function is placed within curly brackets `{}`.

``` js
function name(parameter1, parameter2, parameter3) {
    //code to be executed
}
```

The parameters within the parentheses are also known as arguments. Function arguments are values recieved by the function when it is invoked. Within the function itself the arguments behave as local variables.

Example:

``` js
function toCelsius(fahrenheit) {
    return (5/9) * (fahrenheit-32);
}
```

Here the function name is called `toCelsius` and it takes in a parameter or argument `fahrenheit`. Then the code to be executed is the take whatever value of `fahrenheit` subtract it by 32 and multiply it by the fraction `(5/9)`. Then it will return that value to the function name `toCelsius`.

``` js
console.log(toCelsius(70))
```

Now if I were to type this `console.log` function down the line, it would print the results of the function `toCelsius(70)` to the console. The number 70 would go through the formula written above, and return the correct value.

### Local Variables

``` js
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```

Newly created variables can only be accessed from within the function.
