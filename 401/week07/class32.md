# Context API-Behaviors

## Questions & Answers

[Scaling Up with Reducer and Context](https://react.dev/learn/scaling-up-with-reducer-and-context)

1. How do useReducer and useContext work together to simplify state management in
a React application?
useReducer allows you to have more control over the state of your application and
useContext allows you to access that state in multiple components without having
to pass it down as a prop.
This can be especially useful when you have nested components that need to access
state. Combining these two hooks can help you avoid prop drilling and make your
code more readable and maintainable. The set up for state management can be a bit
more complex than using useState, but the benefits of using useReducer and useContext
can be worth it in the long run.
