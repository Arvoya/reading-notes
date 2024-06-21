# Application State with Redux

## Questions & Answers

[Dan Abramov's Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)

1. What is the first principle of Redux?
Represent the whole state as a single JS object.
2. What is a store and what do we use our reducers for within that store?
A store is an object that holds the application's state object. Reducers are used
to specify how the state object is transformed by actions.
3. Name three Redux store methods given to us by createStore and describe their use.
getState() - returns the current state of the store.
dispatch() - dispatches an action to change the state.
subscribe() - adds a change listener to the store.
4. Explain to a non-technical recruiter what `combineReducers` does and why it
is useful.
`combineReducers` is a function that combines multiple reducers into a single
reducer function. This is useful because it allows you to break down the
reducer logic into smaller, more manageable pieces.

## Resources

[Worlds Easiest Guide to Redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)

[Testing Reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)

[Redux Docs](https://redux.js.org/)

1. Looking ahead at this module’s course schedule, What do you look forward to
learning?
At the time I was excited to learn how to implement these things and work on React
Native as well
2 What are your learning goals after reading and reviewing the class README?
