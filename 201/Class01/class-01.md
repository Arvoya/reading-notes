# Class 1 Reading assignment

Reading assignment ‘Read01’

## Questions & Answers

1. Compose a short poem describing how HTTP sends data between computers.
Haiku: If I'm a Server, HTTP would ask me, Then I would respond.
2. Describe how HTML, CSS, and JS files are "parsed" in the browser. The browser goes through the HTML file first, if it notices a `<script>` or `<link>` element. It will request the server for those files. Then line by line begin to style the webpage and execute the JS functions.
3. How can you find images to add to a Website? You can google stock images, copy their location address, or download locally linking an asset directory to your repo.
4. How do you create a `String` vs a `Number` in JavaScript? For a string you need to make sure to use quotes, for a number just make sure it is an integer not surrounded by quotes.
5. What is a `Variable` and why are they important in JavaScript? Variables are containers used in JS that hold assigned value types.
6. What is an HTML attribute? An HTML attribute is additional information about the specific element.
7. Describe the Anatomy of an HTML element.
8. What is the Difference between `<article>` and `<section>` element tags? You have opening and closing tags, attributes if necessary, and content in between.
9. What Elements does a "typical" website include?

    ``` html
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

10. How does metadata influence Search Engine Optimization? You can change the title and description of your website where search engines use that information to be displayed.
11. How is the `<meta>` HTML used when specifying metadata? It is typically embedded into the `<head>` element.
12. What is the first step to designing a Website? Ask yourself what you want to accomplish, how will the website aid in your goals, and what needs to be done in what order.
13. What is the most important question to answer when designing a Website? Same as above.
14. Why should you use an `<h1>` element over a `<span>` element to display a top level heading? The `<h1>` element is actual heading element, vs `<span>` is for phrasing content.
15. What are the benefits of using semantic tags in our HTML? It helps us understand the purpose and function of the element.
16. Describe 2 things that require JavaScript in the Browser? Dynamically update content, prompt the user, animate images.
17. How can you add JavaScript to an HTML document? External file, inline the specific HTML element, or internally inside the HTML file.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[Getting Started](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web) \| [How the web works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works) \| [Website Design & Process](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/What_will_your_website_look_like) \| [JavaScript: Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics) \| [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML) \| [Getting Started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started) \| [Document and Website Structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure) \| [Metadata in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML) \| [How to start to design a Website](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Design_and_accessibility/Thinking_before_coding) \| [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics) \| [What is JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

## How the web works

### Clients and servers

![Clients and servers](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works/simple-client-server.png)

#### Clients

are the users to access and use the internet through various devices with web-accessing software like a browser.

#### Servers

are the computers that store the data for webpages, apps, etc. When a client wants access to a webpage, their browser downloads a copy of the data onto the client's device to be displayed in their software.

### Under the hood

Some concepts to be understood how this data travels between the server and client and vice versa.

#### TCP/IP

##### Transmission Control Protocol and Internet Protocol

Both of these are a set of rules and steps that define how data travels across the internet.

#### DNS

##### Domain Name System

The 'Yellow-Pages' of the finding websites. When a user types in a web address like `google.com` the browser first looks at the DNS to find the website's IP address before it can retrieve the website from the server.

#### HTTP

##### Hypertext Transfer Protocol

Rules and steps for the language used while the clients and servers speak to one another.

#### Component Files

Name for the files found within a website. These files fall into two categories:

##### Code Files

HTML, CSS, JS

##### Assets

Collection of images, music, video, documents, etc.

### Step by Step

You type a web address into your browser.

1. Browser goes to the DNS server and finds IP address tied to that name.
2. Browser sends HTTP request message to the server asking to send a copy to the user. This message is sent across your internet connection using TCP/IP.
3. Server receives request, and if approved sends the user a "200 OK" message meaning "Yes, you can see the website." Then processed to follow through with the request.
4. The browser assembles the pieces of data into a complete web page and displays it the user.

### Order of Component Files

1. Browser goes through the HTML file first, acknowledging when it passes over a `<link>` or `<script>` element.
2. When it finds those elements it sends a request back to the server for those corresponding files.
3. The browser creates an in-memory DOM tree from the HTML file. An in-memory CSSOM structure from the CSS file. Then compiles and executes the JavaScript file.
4. As it builds the DOM tree, applies the CSS styles, and executes the JavaScript, the user begins to see the webpage.

## Website Design and Process

1. Plan
    - what is your website about?
    - What information are you presenting?
    - What does your website look like?
2. Sketch your design, Wireframing.
3. Assets
    - Text
    - Color
    - Images (either copy address location, or save locally)

## JavaScript Basics

`JavaScript` is a powerful programming language that adds more of a dynamic experience.

`Variables` are containers that hold on the assigned values.

Data Types:

1. `String` - sequence of text
2. `Number` - integer
3. `Boolean` - true/false
4. `Array` - holds multiple values in a single reference
5. `Object` - blog says this can simply be anything

## Intro to HTML

### What is HTML

HTML - HyperText Markup Language

A markup language that creates the structure of your content. It contains a series of elements you use to wrap different parts of the content so that it looks or acts in a certain way.

### Anatomy of an HTML element

Element with attribute
HTML attribute

Attributes contain additional information about the element that does not need to appear in the content itself. In the image above, class is the attribute name, and editor-note is the attribute value.

The class attribute gives the entire element an identifier that can be used to target it with style information.

Attributes that set a value always have:

A space between it and the element name.
The attribute name followed by an equal sign.
The attribute value wrapped by opening and closing quotation marks.
Nesting
Putting elements inside other elements.

`<p>My cat is <strong>very</strong> grumpy.</p>`

Void elements
Some elements have no content within the tags, and some don’t have a closing tag.

``` html
<img src="images/firefox-icon.png" alt="My test image" />
```

Anatomy of an HTML Document

``` html
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

`<html></html>` - this element wraps all the content on the entire page. Known as the root element. Here it includes the `lang` attribute, setting the language to English.

`<head></head>` - this element acts as a container for all the things that aren’t the content you are showing to your users on the page.

`<meta charset="utf-8" />` - this element sets the characters within the document to UTF-8, which includes most characters from the vast majority of written languages. Just found out it can include Sanskrit.

`<meta name="viewport" content="width=device-width" />` - this viewport element makes sure the page renders at the width of the viewport, preventing mobile browsers from rendering incorrectly.

`<title></title>` - this title element sets the title of your page. It will appear in the browser tab, and used to describe the page when you bookmark it.

`<body></body>` - This contains all the content you want to show your users.

Images
`<img src="images/firefox-icon.png" alt="My test image" />`

This element embeds an image into the website in the position it appears. It does this by the src (source) attribute, which contains the path of the image.

In this example there is the alt (alternative) attribute which gives alternative descriptive text for users who cannot see the image.

Those who are visually impaired can use tools known as ‘screen readers’ to read out the alternative text.
Something has caused a crash causing the image to instead show the alternative descriptive text.
Marking up text
Headings
<!-- 6 heading levels: -->

``` html
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
<h5>my sub-sub-subheading</h5>
<h6>my sub-sub-sub-subheading</h6>
Paragraphs
<p>This is a single paragraph</p>
```

`<p>` - elements are for contain paragraphs of text.

Lists
`<ul>` - unordered lists

`<ol>` - ordered lists

Each item inside the lists is put inside a `<li>` (list item) element.

Example

``` html
<p>Here's a list of some topics I've learned so far</p>

<ul>
  <li>HTML</li>
  <li>Wireframing</li>
  <li>Markdown</li>
</ul>

<p>Look how much I've learned!</p>
```

Links
<a>YouTube</a> - start with the anchor element

<a href="https://www.youtube.com">YouTube</a> - add the href attribute.’

Semantics
Refers to the meaning of a piece of code.

Ask yourself

“What purpose or roles does that HTML element have?”
Would you need to look at the code to understand what the function did?
Benefits
Semantic value is seen within search engine optimization
Screen readers can work more effectively
Finding parts of code will be easier to find
Makes it easier for other developers to jump in where you left off

## Things I want to know more about

CSS structure, organization, and efficiency.