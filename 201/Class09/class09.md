# Class 9 Reading Assignment

Reading assignment 'Read 09'

## Questions and Answers

### HTML

1. Why are forms so important in web development? They allow you to get user input, and have the user directly interact with the website.
2. When designing a form, what are some key things to keep in mind when it comes to user experience? Be sure to use the proper `type` for the `<input>` elements, so streamline the type of data you are looking for.
3. List 5 form elements and explain their importance.

    * `<form>` - container element used to create forms
    * `<label>` - label the type of input you'd like the user to put in, like name or address
    * `<input>` - the area in which the user can put in info
    * `<textarea>` - puts default text in place of the input area
    * `<filedset>` - creates label for a section of the form.

---

### JavaScript

1. How would you describe events to a non-technical friend? Events are changes done by the user like clicking their mouse, hovering over something, when the website finishes loading, etc.
2. When using the `addEventListener()` method, what 2 arguments will you need to provide? You will the type of event and the function you'd like it to perform.
3. Describe the event object. Why is the target within the event object useful? You can use it to create functions that will trigger based off a specified target within the event that you are listening for.
4. What is the difference between event bubbling and event capturing? It is where you specified the event listener to take place and cascade. If it's bubbling it starts from the child element moving upward. If it's capturing, you start at the parent and move downward.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[1st Web Form](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form) \| [Web Form Structure](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form) \| [Introduction to Events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

## Web Forms

A critical point of interaction between a user and a website or application

* `<form>` - container element used to create forms

  * `action` - attribute that defines where the forms data should be sent when submitted
  * `method` - attribute that defines which http method to send the data \(`get` or `post`\)

* `<label>` - element to name the input area: 'Name:', 'Address:', etc.
* `<input>` - element with various `types`
  * `mail`, `text`, `password`, '`tel`, `url`, `search`, `range`, `date`, `month`, `time`, `week`, `color`
* `<textarea>` - element that puts default text inside the area
* `<button>` - element that accepts a `type` attribute of the values: `submit`, `reset`, `button`

### From MDN Web Docs

``` HTML

<form action="/my-handling-form-page" method="post">
  <ul>
    <li>
      <label for="name">Name:</label>
      <input type="text" id="name" name="user_name" />
    </li>
    <li>
      <label for="mail">Email:</label>
      <input type="email" id="mail" name="user_email" />
    </li>
    <li>
      <label for="msg">Message:</label>
      <textarea id="msg" name="user_message"></textarea>
    </li>

    …
  </ul>
</form>

```

## Events & Event Handlers

Events are certain actions that happen to the system.

Examples:

* User selects, clicks, hovers with the cursor
* User uses keyboard
* User resizes or closes browser
* A video is played, paused, or ends
* An error occurs

Event Handlers are a block of code that runs when the event fires.

``` JS

const variableName = document.querySelector(HTML element)

myElement.addEventListener("click", functionA);

```

``` JS
const btn = document.querySelector("button");


btn.addEventListener("click", () => {
  
  document.body.style.backgroundColor = blue;
});

```
