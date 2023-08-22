# Class 7 Reading Assignment

Reading assignment 'Read 07'

## Questions and Answers

### Domain Modeling

1. Explain why we need domain modeling: It's all about creating a structure that helps us organize and work with data in a website or app. This structure gives us a clearer picture of how everything fits together and how different parts talk to each other. For us developers, domain modeling is like our toolkit. It helps us build, maintain, and improve software over time. By figuring out the best way to represent real things and their connections, domain modeling helps us make software that's strong, flexible, and useful for people.

-----------------------------------------

### HTML Table Basics

1. Why should tables not be used for page layouts? HTML Tables should not be used for layout as they reduce accessibility, especially for screen readers. It can produce code being messy making it difficult to maintain.
2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.
    * `<thead>` - semantic element used for table headers
    * `<tbody>` - semantic elements used to wrap other content that isn't in the head or footer of the table
    * `<tfoot>` - semantic element used for table footers

-----------------------------------------

### Introducing Constructors

1. What is a constructor, and what are some advantages to using it? A constructor is a blueprint of code that creates an object. It works to make code less redundant.
2. How does the term `this` differ when used in an object literal versus when used in a constructor? In an object literal is specific to that object. When used in a constructor it will refer to the object being created at that time. A more collective use of this, than the specifics of an object literal.

-----------------------------------------

### Object Prototypes Using A Constructor

1. Explain prototypes and inheritance via an analogy from your previous work experience. In my private practice, I occasionally make an herbal formula for a client. The backbone of the formula is always the same, as it needs to pacify the dosha, kindle agni, rebuild tissue, and neutralize the condition. This is like the prototype when building a function that will create an object. From here, depending on what the client is experiencing, what there constitution is, what tissues are damaged, and how to balance to formula accordingly makes it unique and tailored to the client. This is like inheritance where we use the prototype formula to then build in with specific details.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling) \| [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics) \| [Introducing Constructors](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors) \| [Object Prototypes Using A Constructor](https://ui.dev/beginners-guide-to-javascript-prototype)

## Understanding Domain Modeling

 It's all about creating a structure that helps us organize and work with data in a website or app. This structure gives us a clearer picture of how everything fits together and how different parts talk to each other. For us developers, domain modeling is like our toolkit. It helps us build, maintain, and improve software over time. By figuring out the best way to represent real things and their connections, domain modeling helps us make software that's strong, flexible, and useful for people.

## HTML Tables

HTML Tables should not be used for layout as they reduce accessibility, especially for screen readers. It can produce code being messy making it difficult to maintain.

* `<thead>` - semantic element used for table headers
* `<tbody>` - semantic elements used to wrap other content that isn't in the head or footer of the table
* `<tfoot>` - semantic element used for table footers