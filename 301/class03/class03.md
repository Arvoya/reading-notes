[Module301](../README.md)
# Passing Functions as Props

Reading assignment for Class 03

## Questions & Answers

[React Docs](https://react.dev/learn#rendering-lists)

1. What does .map() return? It returns an array.
2. If I want to loop through an array and display each value in JSX, how do I do that in React? You can use `.map()` to loop through the array 
3. Each list item needs a unique ___. It needs a key.
4. WHat is the purpose of a key? The purpose of the key is keep track of each item in the array. Using the index as the key can create issues when changing or rearranging an array.

[The Spread Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

1. What is the spread operator? Spread operator is a feature in JS that spreads out an array, object, or string.
2. List 4 things that the spread operator can do. It can be used within a function, it can clone an array or object. It can merge objects and arrays. You can also add to an array or object.
3. Give an example of using the spread operator to combine two arrays.

     ``` js
      const part1 = [1, 2];
      const part2 = [3, 4];
      const combined = [...part1, ...part2]; // Output: [1, 2, 3, 4]
    ```

4. Give an example of using the spread operator to add a new item to an array.

    ``` js
      const array = [1, 2, 3];
      const newArray = [...array, 4];
    ```

5. Give an example of using the spread operator to combine two objects into one.


    ``` js
    const obj1 = { a: 1, b: 2 };
    const obj2 = { c: 3 };
    const mergedObj = { ...obj1, ...obj2 }; // Output: { a: 1, b: 2, c: 3 }
    ```

[How to Pass A Function As A Prop In React? (Video)](https://www.youtube.com/watch?v=n-6i_WGIOKE)

1. In the video, what is the first step that the developer does to pass functions between components? Create a function handler in the parent component.
2. In your own words, what does the `handleClick` function do? It checks when a user clicks on a DOM element.
3. How can you pass a method from a parent component into a child component? You write the function, and pass down the function as prop.
4. How does the child component invoke a method that passed to it from a parent component? It invokes it as a prop.

## React: Rendering lists

To render a list in React you can use JavaScript features as a `for` loop or the array `map ()` function to create a list of components.

Example:

``` jsx
const fruits = [
  {title: 'Banana', id: 1},
  {title: 'Apple', id: 2},
  {title: 'Blueberry', id:3},
];

// You can use the `map()` function to change the array of fruits into an array of `<li>`.

const listFruits = fruits.map(fruit => 
  <li key={fruit.id}>
    {fruit.title}
  </li>
  );

return (
  <ul>{listItems}</ul>
)
```

### Key Points

* **The `key` Attribute** inside of the `<li>` element is used to identity that item among its siblings. React uses the `key` to be aware if you were to later insert, delete, or reorder the items.
* **Avoid Using Indexes as Keys:** Using indexes can negatively impact performance and lead to issues with component state. This can occur if the list changes. So ensure lists have a stable identity.

## Spread Operator in JavaScript

The spread operator is denoted by `...`. It allows elements of an *iterable* (such as an array or a string) to be expanded or "spread out" into individual elements.

### Key Uses

1. **Function Calls**: Pass array elements as separate arguments to a function.

    ``` js
    const nums = [1, 2, 3];
    const sum = (x, y, z) => x + y + z;
    console.log(sum(...nums)); // Output: 6
    ```

2. **Array Literals**: Create new arrays using existing arrays.

    ``` js
    const part1 = [1, 2];
    const part2 = [3, 4];
    const combined = [...part1, ...part2]; // Output: [1, 2, 3, 4]
    ```

3. **Object Literals**: Combine properties from multiple objects into a new object.

    ``` js
    const obj1 = { a: 1, b: 2 };
    const obj2 = { c: 3 };
    const mergedObj = { ...obj1, ...obj2 }; // Output: { a: 1, b: 2, c: 3 }
    ```

### Additional Insights

* **Shallow Copy:** When using the spread operator with objects, it creates a shallow copy. Nested objects will still be linked to the original object. Any changes will apply to both.

    ``` js
    const original = { a: 1, nested: { b: 2 } };
    const copy = { ...original };
    copy.nested.b = 3;
    console.log(original.nested.b); // Output: 3
    ```

* **Adding New Elements:** The spread operator can be used to add new elements to an existing array.
* **Limitation with Non-Iterable Objects:** The spread works with arrays and object literals, but it cannot be used to spread an object into an array.

### Application Overview

* **Combing Arrays:** You can merge two arrays into a new array.
* **Adding Elements to Arrays:** Easily add new elements to an existing array.
* **Combining Objects:** Merge multiple objects into a single object, combining their properties.
* **Copying Objects:** Create a copy of an object with the same properties.
