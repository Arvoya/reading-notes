[[201/README|Module 201]]
# Class 4 Reading assignment

Reading assignment 'Read 04'

## Questions & Answers

### HTML

1. To create a basic link, we wrap text or other content inside what element? `<a>`
2. The `href` attribute contains what information? It contains the actual web address.
3. What are some ways we can ensure links on our pages are accessible to all readers? In images, we can use the `alt` attribute to describe the image.

-----------------------------------------------------------

### CSS

1. What is meant by "normal flow"? This is the standard layout without any changes.
2. What are a few differences between `block-level` and `inline` elements? Block-level take up an entire row on the webpage, and inline are shaped based on the content size.
3. ___ positioning is the default for every HTML element. Static.
4. Name a few advantages to using absolute positioning on an element. It ensures a specific placement of the element.
5. What is a key difference between fixed positioning and absolute positioning? Fixed will always be in view of the reader. Like a chat box that always stays in the bottom right or left corner. Absolute ignores the placement of anything around it and is only dictated by the space of its parent.

-----------------------------------------------------------

### Learn JS

1. Describe the difference between a function declaration and a function invocation. Declaration of a function is when the function is initially written or created. Invocation of a function is when it is called to execute.
2. What is the difference between a parameter and an argument? An argument is the actual value passed to the function, and parameters are the placeholders in the function's definition that receive those arguments.

-----------------------------------------------------------

### Miscellaneous

1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey. 

    1. Engaged collaboration - I think learning to work well and efficiently with others is a huge perk. Although I'm in a self-paced course, I'm hopeful to work alongside classmates.
    2. Social skills - Being able to effectively communicate, understand, empathize with coworkers can create a healthy work environment and continuously developing those skills can only be beneficial.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[Creating Hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks) \| [CSS Layout: Normal Flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow) \| [CSS Layout: Positioning](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning) \| [Functions - Reusable Blocks of Code](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions) \| [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

## Creating Hyperlinks

### Anatomy of a link

`<a>` - is the element used.
`<href>` - is the attribute that contains the web address (Hypertext Reference).

#### Example

``` html
<p>
  Here is a link to 
  <a href="https://www.youtube.com/">YouTube
  </a>.
</p>
```

### Accessibility Attributes

`title` - within the `<a>` element, can contain additional information about the link
`alt` - used within images can aid in accessibility for those who are unable to view the image as intended.

## CSS

### Normal Flow

They way content or elements from an HTML file are naturally laid out without any modification is known as normal flow. In Code Fellows, they have us reset the entire layout that may be different within various web browsers.

### Positioning

This is the act of taking things out of 'Normal Flow' and changing the positioning of the elements.

There are a couple position properties in CSS:

* Absolute: Positions an element based on its closest positioned ancestor or the initial containing block, allowing it to be taken out of the normal document flow.
* Fixed: Fixes an element's position relative to the viewport, so it remains in a fixed position even when scrolling.
* Static: This is the default position property, and it positions elements in their normal flow order without any special positioning.
* Relative: Positions an element relative to its normal position, while still affecting the layout of other elements around it.

## Functions - Reusable blocks of code

Declaring a function is when code is written that creates the function name and the commands it will execute.

Calling a function is when you write the name along with the parenthesis telling the computer to execute the function.

### Parameters & Arguments

``` JS
function functionName(parameter) {
    // code to execute
}

functionName(argument);
```
