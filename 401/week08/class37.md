# Redux - Combine Reducers

## Questions & Answers

[Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)

1. Why create multiple reducers?
There are different parts of the state that may need to be managed by various
compoennts. Having multiple reducers with different actions help manage this.
2. How would you combine multiple reducers?
You can use the `combineReducers` function from Redux.
3. How will you manage state as an immutable object? why?
You can overwrite the entire state object  with a destructured copy of the
state object and the new state object. This is important because it helps
prevent bugs and makes it easier to track changes.

---

[Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)

1. `combineReducers` is a utility function to simplify the most common use case
when writing ___ _____ .
Redux Reducers
2. Explain how combineReducers assembles the new state tree.
Calls each slice reducer with its current slice of state and current action. It
combines the results into a single object.
3. How would you define initial state in an app using combineReducers?
You can define the initial state in each reducer function.

---

[Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)

1. Why will you want to split your reducing functions as your app becomes more complex?
Becuase it makes it easier to manage the specific part of state with the actions
associated with that part of state.
2. The _____ helper function turns an object whose values are different reducing
functions into a single reducing function you can pass to ____.
`combinereducers`, `configureStore`
3. What is a popular convention when naming reducers?
To name them after the slice of state they manage.

---

1. What are your learning goals after reading and reviewing the class README?
I am looking forward to using multiple reducers in my own projects.
