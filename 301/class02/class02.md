[[301/README|Module 301]]
# State and Props

Reading assignment for Class 02

## Questions & Answers

[React: Component Lifecycle Events](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

1. Based off the diagram, what happens first, the 'render' or the 'componentDidMount'? Render happens first
2. What is the very first thing to happen in the lifecycle of React? Constructor
3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`
    1. `constructor`
    2. `render`
    3. `componenetDidMount`
    4. `React Updates`
    5. `componentWillUnmount`
4. What does `componentDidMount` do? Called after the component is mounted to the DOM initializing DOM elements.

[React State vs Props (Video)](https://www.youtube.com/watch?v=IYvD9oBCuJI)

1. What types of things can you pass in the props? You can pass properties of an html element. You can store any data type.
2. What is the big difference between props and state? Props is input coming in externally. State has internal input change.
3. When do we re-render our application? We re-render when a component has a change.
4. What are some examples of things that we could store in state? You can store any data type.

## React: Component Lifecycle Events

Components can be defined as classes or functions.

**Three phases of the component lifecycle:**

* Mounting - When a component is being created and inserted into the DOM.
* Updating - Occurs when a component is updated or its state changes.
* Unmounting - When a component is being removed from the DOM.

![React Lifecycle Events](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*0saPKFiTUk6W3FYp)
>Sourced from [blog](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

### Lifecycle Methods

A component is being created and inserted into the DOM.

#### Mounting Phase

1. `constructor()`
2. `static get Derived StateFromProps`
3. `render()`
4. `componentDidMount()`
5. `UNSAFE_componentWillMount`

#### Updating Phase

1. `static get DerivedStateFromProps`
2. `shouldComponentUpdate`
3. `render()`
4. `getSnapshotBeforeUpdate`
5. `componentDidUpdate`
6. `UNSAFE_componentWillUpdate`
7. `UNSAFE_componentWillReceiveProps`

#### Unmountaing Phase

1. `componentWillUnmount()`

### Key Points

* **Constructor:** Called before mounting, used for setting state and binding methods.
* **getDerivedStateFromProps:** Used when state depends on changes in props.
* **render():** Required method, examines props and state, should not modify state or directly interact with the browser.
* **componentDidMount():** Called after a component is mounted, good for network requests and DOM initialization.
* **Updating Methods:** Include lifecycle events during the component update due to state or prop changes.
* **componentWillUnmount():** Cleans up the component, good for unsubscribing from network requests.
* **UNSAFE Lifecycle Events:** To be used with caution as they can lead to bugs and unintended side effects.

## State and Props Video

### Props

* **Nature:** Similar to function arguments, passed into a component.
* **Characteristics:**
  * Unchanging within the component.
  * Triggers rerender when changed externally.

### State

* **Nature:** Managed inside the component, dynamic.
* **Characteristics:**
  * Mutable, can be updated within the component.
  * Causes component rerender upon internal changes.

### Comparison

* **Data Management:**
  * Props are handled outside the component.
  * State is handled and updated within the component.
* **Use Cases:**
  * Use props for static data that the component displays.
  * Use state for dynamic data that the component updates based on user interactions.
