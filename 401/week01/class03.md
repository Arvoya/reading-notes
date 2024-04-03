# Express REST API

Reading assignment 'Read 03'

## Questions & Answers

[Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

1. Classes are a template for creating ____.
        Objects
2. Classes are considered ____-based.
        I found multiple answers, but "prototype" makes sense based on the fact
        that classes are templates for objects
3. Can a class declaration be hoisted?
        They behave like they are not hoisted
4. How would you describe a constructor and a contextual 'this' to a non-technical
friend?
        The constructor is a place holder, where it creates an object when called
        upon. So 'this' refers to the name/object that is then being created

---

[Using Express Routing](https://expressjs.com/en/guide/routing.html)

1. Within Express, what does routing refer to?
        They way app's endpoints (URIs) respond to client requests
2. What is the difference between a route path and a route method?
        Route method comes from the HTTP method (GET, POST, PUT, DELETE), and route
        path is the URL.
3. When is it appropriate to add `next` as a parameter to a route handler and what
must you do if `next` has been passed to your middleware as a parameter?
        You add `next` when you want to pass control over to the next middleware
        in the stack. If you have `next` as a parameter, you must call `next()`
        to pass control to the next middleware in the stack.

---

[Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

1. What is an Express Router?
        A miniature version of an express application
2. By what mean do we initialize `express.Router()` in an express server?
        `const router = express.Router();`
3. What do we use route middleware for?
        To guide the request through a series of functions

---

## Reflection

1. What are you learning goals after reading and reviewing the class [README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-03/)?
        Working with SQL databases is something I have not done before, so I am
        looking forward to learning about that. I am also looking forward to
        about making Express servers more efficient.
