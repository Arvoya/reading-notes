# HTML

Reading assignment 'Read04'

## Questions & Answers

1. What is HTML and why do we use it? HTML is a markup language that defines the structure of content on web pages. It consists of elements used to enclose various parts of content, allowing them to be presented or behave in specific ways.
2. What are the 3 main parts of an HTML element? An HTML element has three main parts: the opening tag, which marks the beginning of the element; the content, which is the actual data enclosed by the element; and the closing tag, which signifies the end of the element.
3. What is it called when you give an element extra information? Providing additional information to an element is known as adding an attribute. Attributes enhance the element's behavior or presentation without altering its core content.
4. What is a semantic element? A semantic element is a specific type of HTML tag that carries meaning about the role or purpose of the enclosed content. Semantic elements contribute to the structure and understanding of a web page's content by describing its significance to both browsers and developers.

## Notes

Here are the notes I've taken while reading the following blogs:

[Wireframe & Design](https://careerfoundry.com/en/blog/ux-design/how-to-create-your-first-wireframe/) \| [Mozilla HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) \| [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)

## Wireframe & Design

### Wireframing

A practice that designs the rudementary layout of the various pages used in a website. It let syou plan the layout and interaction of your webpage.
>...if a user doesn’t know where to go on a plain hand-drawn diagram of your site page, then it is irrelevant what colors or fancy text eventually get used. A button or call to action needs to be clear to the user even it’s not brightly colored and flashing.

### Tips for complete beginners

- Drawn wireframes are easy to change and aid in early converstaions about your website or product
- Using paper-prototypes allow you to test with users at every stage of ideation and design.
- Switching to software later on lets you keep track of details


### Wireframes from CareerFoundry student Samuel Adaramola
![examples](https://d3mm2s9r15iqcv.cloudfront.net/en/wp-content/uploads/old-blog-uploads/versions/samuel-student-wireframe---x----972-715x---.png)

### 6 Steps to make a wireframe

1. Do your research
    - understand who your audience is
    - create user personas and define use cases
2. Prepare research for quick reference
    - create a cheetsheet that contains
      - business & user goals
      - personas
      - use cases
      - cool features
3. Have user flow mapped out
    - How many screens will you need
    - Where are you users coming from?
    - Where do you need them to end up?
    - How can you organise the content to support your users’ goals?
    - Which information should be most prominent? Where should your main message go? What should the user see first when arriving at the page?
    - What will the user expect to see on certain areas of the page?
    - Which buttons or touch points does the user need to complete the desired actions?
4. Draft, don't draw. Sketch, don't illustrate
    - "look before you leap"
5. Add some detail and test
    - Add detail in the way you would naturally process a screen, or the page of a book: from top-to-bottom and left-to-right
    - Simple, instructional wording for i.e. calls-to-action
    - Trust-building elements: What do you need to build trust in your customers and where would be the best place to put these elements?
6. Prototypes
    - A working model of an app or webpage.
    - Test the user journey
    - My program of choice - Adobe Xd

### 3 Principles

1. Clarity
2. Confidence
3. Simplicity

## Mozilla HTML Basics

### What is HTML

HTML - HyperText Markup Language

A markup language that creates the structure of your content. It contains a series of elements you use to wrap different parts of the content so that it looks or acts in a certain way.

### Anatomy of an HTML element

![html element](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)

### Element with attribute

![HTML attribute](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-attribute-small.png)

Attributes contain additional information about the element that does not need to appear in the content itself. In the image above, `class` is the attribute name, and `editor-note` is the attribute value.

The `class` attribute gives the entire element an identifier that can be used to target it with style information.

Attributes that set a value always have:

1. A space between it and the element name.
2. The attribute name followed by an equal sign.
3. The attribute value wrapped by opening and closing quotation marks.

### Nesting

Putting elements inside other elements.

`<p>My cat is <strong>very</strong> grumpy.</p>`

### Void elements

Some elements have no content within the tags, and some don't have a closing tag.

`<img src="images/firefox-icon.png" alt="My test image" />`

### Anatomy of an HTML Document

``` HTML
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>My test page</title>
  </head>
  <body>
    Hello World! ॐ
  </body>
</html>
```

`<!doctype html>` - is a required piece of code that is needed to make sure your document behaves correctly.

`<html></html>` - this element wraps all the content on the entire page. Known as the root element. Here it includes the lang attribute, setting the language to English.

`<head></head>` - this element acts as a container for all the things that aren't the content you are showing to your users on the page.

`<meta charset="utf-8" />` - this element sets the characters within the document to UTF-8, which includes most characters from the vast majority of written languages. Just found out it can include Sanskrit.

`<meta name="viewport" content="width=device-width" />` - this viewport element makes sure the page renders at the width of the viewport, preventing mobile browsers from rendering incorrectly.

`<title></title>` - this title element sets the title of your page. It will appear in the browser tab, and used to describe the page when you bookmark it.

`<body></body>` - This contains **all** the content you want to show your users.

### Images

`<img src="images/firefox-icon.png" alt="My test image" />`

This element embeds an image into the website in the position it appears. It does this by the `src` (source) attribute, which contains the path of the image. 

In this example there is the `alt` (alternative) attribute which gives alternative descriptive text for users who cannot see the image.

- Those who are viusally impaired can use tools known as 'screen readers' to read out the alternative text.
- Something has caused a crash causing the image to instead show the alternative descriptive text.

### Marking up text

#### Headings

``` HTML
<!-- 6 heading levels: -->
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
<h5>my sub-sub-subheading</h5>
<h6>my sub-sub-sub-subheading</h6>
```

#### Paragraphs

`<p>This is a single paragraph</p>` 

`<p>` - elements are for contain paragraphs of text.

#### Lists

`<ul>` - unordered lists

`<ol>` - ordered lists

Each item inside the lists is put inside a `<li>` (list item) element.

##### Example

``` HTML
<p>Here's a list of some topics I've learned so far</p>

<ul>
  <li>HTML</li>
  <li>Wireframing</li>
  <li>Markdown</li>
</ul>

<p>Look how much I've learned!</p>

```

### Links

`<a>YouTube</a>` - start with the **a**nchor element

`<a href="https://www.youtube.com">YouTube</a>` - add the `href` attribute.'

## Semantics

Refers to the meaning of a piece of code.

Ask yourself 
- "What purpose or roles does that HTML element have?"
- Would you need to look at the code to understand what the function did?

### Benefits

- Semantic value is seen within search engin optimization
- Screen readers can work more effectively
- Finding parts of code will be easier to find
- Makes it easier for other devlopers to jump in where you left off