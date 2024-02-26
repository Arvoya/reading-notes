[Module301](../README.md)
# React & Higher Functions

Reading assignment for Class 05

## Questions & Answers

[React Docs - Thinking in React](https://react.dev/learn/thinking-in-react)

1. What is the `single responsibility principle` and how does it apply to components? That a component should only do one thing.
2. What does it mean to build a 'static' version of your application? Build the application but it doesn't have any user input or reactivity based off of that input.
3. Once you have a static application, what do you need to add? You will need to add states within the components for it keep track of user input.
4. What are the three questions you can ask to determine if something is state?
    1. Does it remain changed overtime?
    2. It is passed from a parent via props?
    3. Can you compute it based on existing state or props in your component?
5. How can you identify where state needs to live? Find our which component is responsible for changing the state.

[Higher - Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

1. what is a "higher-order function"? A function that takes one or more functions as arguments, or returns a function as its result.
2. Explore the `greaterThan` function as defined in the reading. In your own words, what is line 2 of this function doing? It is returning a boolean statement by comparing if the argument is a greater value than the function created.
3. Explain how either `map` or `reduce` operates, with regards to higher-order functions. `map` works by applying a function to each element within an array and returns a new array with the returned value from the function passed as the argument. `reduce` works in a similar way that it takes a function as an argument, but instead of returning an array it returns an individual value.

## Thinking in React

Steps to build a UI with React

1. Break the UI into a component hierarchy
2. Build a static version in React
3. Find the minimal but complete representation of UI state
4. Identify where your state should live
5. Add inverse data flow

### Component Hierarchy

Draw boxes around every component and subcontinent, and name them.
he design in different ways:

1. **Programming** - A component should ideally only do one thing. Known as 'single responsibility principle'.
2. **CSS** - Consider what you would make class selectors for.
3. **Design** - consider how you would organize the design's layers.

Remember that components that appear within another component in the mockup should appear as a child in the hierarchy.

### Static Version

Build a version of your app that renders the UI from the data model but doesn't have any interactivity.

Build your components that reuse other components and pass data using props. Do not use state yet as it reserved for interactivity.

### Minimal UI Representation State

Let users change your underlying data model.

Important to remember DRY - Don't Repeat Yourself

### Identify State Placement

Figure out which component is responsible for changing this state.

For each state:

1. Identify *every* component that renders something based on that state.
2. Find their closest common parent component - a component above them all in the hierarchy.
3. Decide where the state should live:
    1. Directly into their common parent.
    2. Above their common parent.
    3. Create a new component solely for holding the state.

### Add Inverse Data Flow

Now that props and state are flowing down the hierarchy, you need to let user input change state by supporting data flowing up the hierarchy.

## Order Functions

### Abstraction

> Abstractions hide details and give us the ability to talk about problems as a higher (or more abstract) level.

### Higher-Order Functions

A function that either takes one or more functions as arguments or returns a functions as its result.

Higher-order functions allow us to abstract over *actions*, not just values.

#### Creating New Functions

This function will create new functions that can check if the value is higher than what was initially created.

``` JavaScript
function greaterThan(n) {
  return m => m > n;
}

let greaterThan10 = greaterThan(10);

console.log(greaterThan10(9));

// the return will be false because 9 is not greater than 10
```

#### Functions That Change Other Functions

This `noisy` function can take other functions `f` a even make use of the function it called. In this example it takes in the function `Math.min` which find the lowest number value. `noisy` also takes in an array `3, 2, 1` the function `noisy` then runs the function `Math.min` and uses the array as the argument for the `Math.min` function. Thus returning 1.

``` JavaScript
function noisy(f) {
  return (...args) => {
    console.log("calling with", args);
    let result = f(...args);
    console.log("called with", args, "returned", result);
    return result;
  };
}

noisy(Math.min)(3, 2, 1);

/* Expected Logs:
calling with [3, 2, 1]
called with [3, 2, 1] returned 1
*/

```

### Transforming with Map

> The `map` method transforms an array by applying a function to all of its elements and building a new array from the returned values.

``` JavaScript
function map(array, transform) {
  let mapped = [];
  for (let element of array) {
    mapped.push(transform(element));
  }
  return mapped;
}

let exampleArray = [1, 2, 3];

let newArray = exampleArray.map(element => element * 2);

console.log(newArray);

/* Expected Logs:
[2, 4, 6];
*/
```

### Summarizing With Reduce

Sometimes called *fold*, reduce is where you take an array, apply a function to combine the array, and include a starting value.

In the example below, `reduce()` is taking combing all the values of an array.

``` JavaScript
function reduce(array, combine, start) {
  let current = start;
  for (let element of array) {
    current = combine(current, element);
  }
  return current;
}

console.log(reduce([1, 2, 3, 4], (a, b) => a + b, 0));
// → 10
```
