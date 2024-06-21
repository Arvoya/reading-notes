# Advanced State with Reducers

## Questions & Answers

[Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)

1. What is the motivation for adding a reducer?
When you start working on a larger project where state can be hard to visualize,
a reducer can help you manage state more effectively.
2. What are actions in the context of a reducer? How are they different than setting
state directly?
Actions are specific ways to change state. When you set state directly within a
component, you are using various funcitons. Actions are more specific and can be
exported/imnported to be used in mulitple places.
3. What common list operation is useReduce named for, and why?
Named for the reducer function that will be used to update state.
4. When should you switch from useState to useReducer?
When you start to have more complex state that needs to be managed in multiple
places.

---

1. What are your learning goals after reading and reviewing the class README?
This was super cool to learn, and have been using this in my own projects. I
find it much easier to manage state with reducers.
