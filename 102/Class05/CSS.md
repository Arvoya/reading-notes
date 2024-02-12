[[102/README|Module 102]]
# CSS

Reading assignment 'Read05'

## Questions & Answers

1. What is the purpose of CSS? To style the webpage for a desired outcome.
2. What are the three ways to insert CSS into your project? Internal, External, Inline
3. Write an example of CSS rule that would give all `<p>` elements red text.
- **Internal example**

``` HTML
<p style="color:red;">This text will be red</p>
```

- **External example**

``` CSS
p {
    color: red;
}
```

- **Inline example**

``` HTML
<!DOCTYPE html>
<html>
    <body>

        <p style="color:red;">This text will be red</p>

    </body>
</html>
```

## Notes

Here are the notes I've taken while reading the following blogs:

[What is CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS) \| [How to add CSS](https://www.w3schools.com/css/css_howto.asp) \|

## What is CSS

**CSS** - Cascading Style Sheets

> CSS allows you to create great-looking web pages

### CSS Syntax

CSS is a rule-based language, meaning you define rules by specifying groups of styles that should be applied to particular HTML elements.

#### Example

``` CSS
h1 {
    color: red;
    font-size: 5em;
}
```

- `h1` is the selector. This selects the HTML element `h1` and styles it.
- Inside the curly braces `{}`, one or more declarations will be defined.
  - Declarations are made up of a property and its corresponding value. In this case, the properties are `color` and `font-size`, and the values are `red` and `5em`, respectively.

CSS properties can take in a variety of values depending on which property is being used. In the example of color, there are a wide range of colors to choose from and ways of inputing the color.
- you can use an RBG format of `rgb(255,255,255)`
- or a Hex Code `#000000`

### CSS Modules

Because of the various ways using CSS can style a web page. The language itself is broken down into modules. You can use references of these modules to find a wide range of properties.

Example Module: [Backgrounds & Borders](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_backgrounds_and_borders)

These are just some of the propteries under this module:

- `background-attachment`
- `background-clip`
- `background-color`
- `background-image`
- `background-origin`
- `background-position`
- `background-repeat`
- `background-size`
- `border-collapse`
- `border-bottom-left-radius`
- `border-bottom-right-radius`
- `border-top-left-radius`
- `border-top-right-radius`

### CSS Specifications

All of the web technologies like (HMTL, CSS, JavaScript, etc) are standarized and published by organzations such as: [W3C](https://www.w3.org/), [WHATWG](https://whatwg.org/), [ECMA](https://www.ecma-international.org/), or [Khronos](https://www.khronos.org/). These compaines define exactly how these technologies are suppose to act and behave.

## How to Add CSS

### 3 ways to interst CSS

1. External CSS
2. Internal CSS
3. Inline CSS

### External CSS

By using an external style sheet, you can change the look of an entire website within a single file.

The HTML page must include a reference to the external style sheet file inside the `<link>` element, inside the head section.

**Example:**

``` HTML
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <h1>This is a heading</h1>
        <p>This is a paragraph.</p>
    </body>
</html>
```

The external style sheet can be written in any text editor and must use the '.ccs' extension.

**Example of a style.css file:**

``` CSS
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```

### Internal CSS

An internal style sheet is the act of writting CSS syntax within the same HTML document.

To do so the internal style is defined inside of the HTML `<style>` element. This element must also be nested inside of the `<head>` element.

**Example:**

``` HTML
<!DOCTYPE html>
<html>
    <head>
        <style>
            body {
            background-color: linen;
            }       

            h1 {
            color: maroon;
            margin-left: 40px;
            }
        </style>
    </head>
    <body>

        <h1>This is a heading</h1>
        <p>This is a paragraph.</p>

    </body>
</html>
```

### Inline CSS

An inline style is used to style a single element within an HTML file.

**Example**

``` HTML
<!DOCTYPE html>
<html>
    <body>

        <h1 style="color:blue;text-align:center;">This is a heading</h1>
        <p style="color:red;">This is a paragraph.</p>

    </body>
</html>
```

> **Tip:** An inline style loses many of the advantages of a style sheet (by mixing content with presentation). Use this method sparingly.

### Cascading Order

All the styles in a page will "cascade" into a new *virtual* style sheet by the following these rules in order.

1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default