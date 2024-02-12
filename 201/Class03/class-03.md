[[201/README|Module 201]]
# Class 3 Reading assignment

Reading assignment 'Read 03'

## Questions & Answers

1. When should you use an `unordered list` in your HTML document? When you don't require numbers or Roman numerals to dictate an order for the list.
2. How do you change the `bullet style` of unordered list items? It's suggested to use the CSS property `list-style-type`.
3. When should you use an `ordered list` vs an `unorder list` in your HTML document? When you require the list to be a certain order where it is required to have numbers or Roman numerals.
4. Describe two ways you can change the numbers on `list items` provided by an `ordered list`? Using the attributes `type` along with `a`, `A`, `i`, or `I` will change the character used. Another way is to change the order it starts at using the `start` element and giving it a number to start at.
5. Describe the CSS properties of `margin` and `padding` as characters in a story. What is their role in a story titled: "The Box Model"? Margin are Padding are fundamental forces of nature in the universe known as Box. Padding was more of a microcosm to the macrocosm nature of Margin. Padding would be the field surrounding all the content in the universe. While Margin does the same at a much greater scale. If padding was the water between islands in a planet. Margin is the celestial river between galaxies.
6. List and describe the four parts of an HTML elements box as referred to by the `box model`.

    * Content box - area where content is displayed
    * Padding box - sits around the content as white space
    * Border box - wraps the content and any padding
    * Margin - outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements

7. What `data types` can you store inside an `Array`? All types!
8. Is the `people` array a valid JavaScript array? If so, how can I access the values stored? If not, why?
It is possible to access the values stored by using a pair of brackets.

    * `people[0][1]` would give you the number 32.

    ``` js
    const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];
    ```

9. List **five** shorthand operators for assignment in JavaScript and describe what they do.

    | Operator | Example | Description |
    |----------|---------|-------------|
    | =        | x = y   | variable x equals variable y
    | +=       | x += y  | variable x equals x plus the variable y
    | -=       | x -= y  | variable x equals x minus the variable y
    | *=       | x *= y  | variable x equals x times the variable y
    | /=       | x /= y  | variable x equals x divided by the variable y

10. Read the code below and evaluate the last `expression` and explain what the result would be and why. Learning that 0 would take place of false. The first part of the equation would be 10+0 equating to 10. Then 10 plus `dog` would equate to `10dog`.

    ``` js
    let a = 10;
    let b = 'dog';
    let c = false;
    // evaluate this
    (a + c) + b;
    ```

11. Describe a real world example of when a conditional statement should be used in a JavaScript program. In the use of requiring a specific password, a conditional statement would be very useful.
12. Give an example of when a `Loop` is useful in JavaScript. A loop is useful when you require code to repeat itself without the need to re-write the code however many times you need it to run.

## Notes

Here are the notes I’ve taken while reading the following blogs:

* HTML [Ordered List](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) \| [Unordered List](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)
* CSS [The Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
* JS [Arrays](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays) \| [Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) \| [Conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals) \| [Loops](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)

## Ordered List

`<ol>` - element used to create a list rendered as a numbered list.

### Attributes

* `revered` - this will list the items from high to low
* `start` - you can change the starting number of a list
* `type` - sets the numbering type
  * `a` for lowercase
  * `A` for uppercase
  * `i` for lowercase Roman numerals
  * `I` for uppercase Roman numerals
  * `1` for numbers (default)

### Nesting

Example:

``` html
<ol>
  <li>first item</li>
  <li>
    second item
    <!-- closing </li> tag is not here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
  </li>
  <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>
```

## Unordered List

`<ul>` - element used to create a list rendered as a bulleted list.

### Attributes vs CSS

It's better to use a CSS styling property than attributes for the HTML element. Nesting works the same regardless if its ordered or unordered.

## The Box Model

In CSS, elements are represented as boxes, which are categorized into 'block boxes' and 'inline boxes.'

Examples:

* `<h1>` s an example of a block-level element, creating a block-level box.
* `<a>`is an example of an inline-level element, creating an inline-level box.

From here, each box has an 'inner display type' and an 'outer display type'.

* Inner Display Type: This refers to how the content inside the box is organized and displayed. For instance, within a block-level box, such as a `<h1>`, the inner display type determines how the contained elements, like text and images, are laid out within the box.
* Outer Display Type: This pertains to how the box itself interacts with other boxes on the page. It influences the box's positioning in relation to neighboring elements, as well as how content flows around it. For instance, the outer display type of a block-level box affects its vertical arrangement and the space it occupies within the layout.

### What is the CSS box model?

#### Parts of a box

* Content box - area where content is displayed
* Padding box - sits around the content as white space
* Border box - wraps the content and any padding
* Margin - outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements

## Arrays

Arrays are 'list-like objects' that can be stored within a single variable. The data-types within an array can vary. There are many ways to edit an array, pull out a specific object within an array, or add to one if needed.