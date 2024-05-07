# Component Based UI

## Questions & Answers

[React Quick Start](https://react.dev/learn)

1. What are the building blocks of a React app?
Components
2. What is the difference between an HTML element and a React component?
HTML elements are static and can't include javascript. React components are dynamic and can include javascript.
3. What is JSX and why do we use it?
JSX is a syntax extension for JS and it allows us to write HTML elements in JS.
4. Describe the process of embedding JavaScript expression in JSX?
You have to wrap the expression in curly braces `{}`.
5. Does React or JSX have an special features for iteration or conditional logic?
No major differences.
6. How does React know to respond to a user's inputs?
React uses state to keep track of the user's input.
7. What word indicates that React component manages data with a Hook?
`useState`
8. How can two react components share data?
By passing props from one component to another.

---

[Render and Commit](https://react.dev/learn/render-and-commit)

1. What are the three steps of refreshing a React UI?
Triggering, Rendering, Committing
2. How do you trigger updates to a component after the initial render?
By updating state
3. Does React recreate DOM nodes on every rerender?
No, it only updates the components that have changed.
4. After React has updated the DOM, what still needs to happen before the user sees
the change?
The browser needs to `paint` the changes to the screen.

## Resources

[Your First Component](https://react.dev/learn/your-first-component)
[Importing and Exporting Components](https://react.dev/learn/importing-and-exporting-components)
[Writing Markup with JSX](https://react.dev/learn/writing-markup-with-jsx)
[sass cheatsheet](https://devhints.io/sass)
[react cheatsheet](https://devhints.io/react)

## Additional Questions

1. Note the naming conventions in the [Airbnb React/JSX Style Guide.](https://airbnb.io/javascript/react/#naming)
What pattern(s) do you see?
It tries to keep the naming conventions consistent and easy to read.
2. Looking ahead at this module's [course schedule,](https://codefellows.github.io/code-401-javascript-guide/curriculum/#module-6)
What do you look forward to learning?
React Native really interests me as I want to be understand how to make mobile apps.
3. What are your learning goals after reading and reviewing the [class README?](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-26/)
Components loading their own css seems really interesting, and today we also went
over some typescript, so that is exciting.
