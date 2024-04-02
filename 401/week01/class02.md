# Express, NPM, TDD, CI/CD

Reading assignment 'Read 02'

## Questions & Answers

[An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)

1. Explain middleware, answer as though I were a non-technical recruiter.
        Middleware is a functional way for different parts of a system to communicate
        or exchange data.
2. Express the most popular ______.
        Node web framework.
3. Express is "un-opinionated." What does that mean?
        It means that Express does not enforce a specific way of doing things.
4. What is a module and why is modularity useful to us as developers?
        A piece of software that is used within other software. Modularity
        allows for code reuse and easier maintenance.

---

[What is NPM?](https://docs.npmjs.com/getting-started/what-is-npm)

1. What version of npm are you running on your machine?
        10.5.0
2. What command would you type to install a library/package called 'jshint' into
your node project?
        `npm install jshint`

---

[What is TDD?](https://www.agilealliance.org/glossary/tdd/)

1. Explain why tests are important. Please explain as though I were your non technical
elder.
        Test are important because they help us understand if our code is working.
        Every time we write new code, we should write a test to make sure it works.
        This way we can be sure that our code is working as expected.
2. What are three expected benefits of testing?
        - Teams report that they catch less bugs
        - Teams report that the time to write tests is less than the time to fix
        bugs
        - Improvement of quality
3. Name at least 2 individual pitfalls and at least 2 team pitfalls commonly encountered
while writing tests.
        - Individual pitfalls:
            - Writing tests after the code
            - Writing tests that are too complex
        - Team pitfalls:
            - Only a few team members write tests
            - Poor quality in writing tests

---

[CI/CD](https://www.youtube.com/watch?v=k2aNsQKwyOo)

1. What are three benefits of Continuous Integration?
        - Less bugs
        - Faster development
        - Better quality
2. What is the difference between Continuous Delivery and Continuous Deployment?
        - Continuous Delivery: The code is automatically deployed to a staging
        environment after passing the tests.
        - Continuous Deployment: The code is automatically deployed to production
        after passing the tests.
3. Explain how GitHub fits into this process assuming the listener comes from a
non-technical background
        GitHub is a platform where developers store all of their code. It is
        used to store the code and to collaborate with other developers. So it
        is the hub where everyone can both do CI/CD and store their code.
