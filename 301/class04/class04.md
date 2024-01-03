# React Forms & Ternary Operator

Reading assignment for Class 04

## Questions & Answers

[How to use Forms in React](https://www.robinwieruch.de/react-form/)

1. What is a 'Controlled Component'? A controlled component is a way to handle the values that are submitted in React forms, where the input is saved into a React state and then updated to the UI.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why. In controlled components, you can update the state with user responses as they enter for real-time validation and dynamic feedback. If it's a really big form, you can opt to wait until submission with an uncontrolled component.
3. How do we target what the user is entering if we have an event handler on an input field? We use the `onChange` handler to update the state or use `ref` to access input directly from the DOM.

[The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

1. Why would we use a ternary operator? To write more concise and 1 liner code.
2. Rewrite the following statement using a ternary statement:

  ``` JavaScript
  if(x===y){
  console.log(true);
  } else {
    console.log(false);
  }
  ```

  ``` JavaScript
  
  x === y ? console.log(true) : console.log(false);
  
  ```

## React Forms

Two primary ways to manage forms: Controlled and Uncontrolled components.

### Controlled Components

Controlled components are those where the form data (input values) are managed by the component's state.

Input values are set by state variables, and changes are captured through event handlers like `onChange`. UI stats in sync with the user's input.

Ideal for real-time validation, enforcing input formats, or dynamically handling changes.

Example:

``` jsx
// Functional Component
const [inputValue, setInputValue] = React.useState('');

const handleInputChange = (event) => {
  setInputValue(event.target.value);
};

// Class Component
class ExampleComponent extends React.Component {

  constructor(props) {
    super(props);
    this.state = { inputValue: '' };
  }

  handleInputChange = (event) => {
    this.setState({ inputValue: event.target.value });
  };

  render() {
    return (
      <input
        type="text"
        value={this.state.inputValue}
        onChange={this.handleInputChange} // Using arrow function
      />
    );
  }
}


```

### Uncontrolled Components

Uncontrolled components manage form data directly through the DOM, using refs (`useRef` in functional components and `createRef` in class components).

Instead of state, uncontrolled components use refs to directly interact with the DOM elements. The form data is accessed as needed - during form submission.

Suitable for simple forms where direct DOM manipulation is preferred. Or when integrating with non-React code.

Example:

``` jsx
// Functional Component
const inputRef = React.useRef();

const handleSubmit = (event) => {
  event.preventDefault();
  console.log(inputRef.current.value);
};

// Class Component
class ExampleComponent extends React.Component {

  constructor(props) {
    super(props);
    this.inputRef = React.createRef();
  }

  handleSubmit(event) {
    event.preventDefault();
    console.log(this.inputRef.current.value);
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit.bind(this)}>
        <input type="text" ref={this.inputRef} />
        <button type="submit">Submit</button>
      </form>
    );
  }
}
```

### Form Submission and Event Handling

The `onSubmit` attribute on the form element is used to handle form submission events. It's necessary to prevent the default submission action using `event.preventDefault()` to avoid page reload.

Example:

``` jsx
const handleSubmit = (event) => {
  event.preventDefault();
}
```

### Form Validation

Ensure users inputs meet predefined criteria before form submission.

Can be manually implemented in controlled components or handled through libraries like React Hook Form.

Manual Example:

``` jsx

const LoginForm = () => {
  const [email, setEmail] = React.useState('');
  const [emailError, setEmailError] = React.useState('');

const validateEmail = () => {
  if (!email.includes('@')) {
    setEmailError('Invalid email address');
    return false;
  }
  setEmailError('');
  return true;
};

const handleSubmit = (event) => {
  event.preventDefault();

  if (validateEmail()) {
    // Submit form logic
  }
};

```

## Ternary Operator

Ternary operator is a concise and efficient way to write conditional statements in JavaScript. It's useful for assinging values based on a condition in a single line of code.

**Structure:**

Syntax: condition `?` valueIfTrue `:` valueIfFalse

This operator is ideal for scenarios like JSX in React where inline expressions are needed.

Examples:

- Basic Usage:

  ``` jsx
  let canDrive = age >= 16 ? 'Yes' : 'No';
  ```

- Nested:

  ``` jsx
  let message = age > 18 ? (student ? 'Student over 18' : 'Adult') : 'Underage';
  ```
