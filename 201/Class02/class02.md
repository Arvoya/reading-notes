# Class 2 Reading assignment

Reading assignment 'Read 02'

## Questions & Answers

1. Why is it important to use semantic elements in our HTML? Because they help the programmers understand the function of the element.
2. How many levels of heading are there in HTML? 6
3. What are some uses for the `<sup>` and `<sub>` elements? Math, Science, giving dates.
4. When using the `<abbr>` element, what attribute must be added to provide? Use the `<title>` element to give a full description of the abbreviation or acronym.
5. What are ways we can apply CSS to our HTML? Externally, Internally, or Inline.
6. Why should we avoid using inline styles? It's more difficult to read, not as efficient, and creates a difficult work environment to debug.
7. Review the block of code below and answer the following questions:
    1. What is representing the selector? `h2`
    2. Which components are the CSS declarations? `color: black;` & `padding: 5px;`
    3. Which components are considered properties? `color:` & `padding:`
8. What data type is a sequence of text enclosed in a single quote marks? `string`
9. List 4 types of JavaScript operators.
    1. Addition `+`
    2. Assignment `=`
    3. Not `!`
    4. Strict equality `===`
10. Describe a real world Problem you could solve with a Function. Use a function to quickly convert Fahrenheit to Celsius.
11. An if statement checks a _ and if it evaluates to \_, then code block will execute. *condition*, *true*
12. What is the use of an `else if`? Incase the programmer requires an entirely separate condition to run a specific command.
13. List 3 different types of comparison operators. `<`, `>`, `<=`
14. What is the difference between the logical operator `&&` and `||`? `&&` is checking if both are true. `||` is checking if either is true.

**For Question 7:**

``` css
   h2 {
     color: black;
     padding: 5px;
   }
```

## Notes

Here are the notes I’ve taken while reading the following blogs:

[HTML Text Fundamentals](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals) \| [HTML Advanced Text Formatting](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting) \|[How CSS is structured](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured)

## Advanced text formatting

### Superscript and subscript

Superscript - `<sup>` \| used for mathematical equations or dates of the year.

Subscript - `<sub>` \| used for chemical formulae

### Abbreviations

`<abbr>` - used to wrap around the abbreviation or acronym. Use the attribute `<title>` to prove the full expansion of the term.