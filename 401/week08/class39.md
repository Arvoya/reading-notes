# Redux - Additional Topics

## Questions & Answers

[Redux Toolkit (RTK) Intro](https://redux-toolkit.js.org/introduction/getting-started)

1. What concerns are addressed by Redux Toolkit?
    - "Configuring a Redux store is too complicated"
    - "I have to add a lot of packages to get Redux to do anything useful"
    - "Redux requires too much boilerplate code"
2. What does configureStore() do?
It wraps around `createStore` to provide simplified configuration options and good
defaults
3. How would I use createSlice()?
Accepts an object of reducer functions, slice name, initial state value, and generates
a reducer with corresponding action creators

---

[MobX](https://mobx.js.org/getting-started.html)

1. What is Mobx?
It is another way to manage state in your application
2. How does MobX make it “impossible” to produce an inconsistent state?
It makes sure that everything that can be derived from the application state, will
be derived automatically.
3. How would we build a reactive user interface?
By using the `observer` function from MobX, and making the class that you want to
observe an observer.

---

[Tutorial](https://redux-toolkit.js.org/tutorials/intermediate-tutorial)

1. What take-away(s) did this tutorial provide?
Some of it was review, and a lot of I know I will need to use in projects to fully
understand it. I think the managing of state is incredibly important and can make
or break an application work flow.

## Resources

[Redux Toolkit (RTK)](https://redux-toolkit.js.org/)

[HookState](https://hookstate.js.org/)

1. What are your learning goals after reading and reviewing the class README?
Building our own hooks seem interesting to me and some of us were able to do it
in our final projects which was cool.
