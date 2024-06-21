# Redux - Asynchronous Actions

## Questions & Answers

[async actions](https://redux.js.org/advanced/asyncactions)

1. Why use Redux middleware?
Because it allows you to have actions that can do more than just return an object.
2. Consider the Redux Async Data Flow Diagram. Describe the flow in your own words.
The action creator dispatches an action that is intercepted by the middleware. The
middleware then dispatches the action to the reducer.
3. How are we accommodating async in our Redux app?
By using middleware to intercept the action and dispatch it to the reducer.

---

[thunk middleware](https://github.com/reduxjs/redux-thunk)

1. Why would you need redux-thunk middleware?
 It allows writing functions with logic inside that can interact with a Redux store's
 dispatch and getState methods.
2. Redux Thunk middleware allows you to write action creators that return a ____
instead of an action.
3. Describe how any return value from the inner thunk function will be made available.

---

1. What are your learning goals after reading and reviewing the class README?
