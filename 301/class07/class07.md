# NODE.JS

Reading assignment for Class 07

## Questions & Answers

[An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js/)

1. What is node.js? A JavaScript runtime built on Chrome's V8 engine.
2. In your own words, what is Chrome's V8 JavaScript Engine? It is a compiler within the browser to change JS into machine code.
3. What does it mean that node is a JavaScript runtime? Instead of staying within the browser, JavaScript can now run using the same engine that chrome built outside of the browser. Making it executable within a computer or server.
4. What is npm? It is a package manager.
5. What version of node are you running on your machine? v21.1.0
6. What version of npm are you running on your machine? 10.2.0
7. What command would you type to install a library/package called 'jshint'? npm install jshint
8. What is node used for? It is used to run JavaScript code outside the browser.

[6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

1. What are the 6 reasons for pair programming?
   1. Greater efficiency
   2. Engaged Collaboration
   3. Learning from fellow students
   4. Social Skills
   5. Job Interview Readiness
   6. Work Environment Readiness
2. In your experience, which of these reasons have you found most beneficial? I haven't much pair programming due to the nature of being self-paced, but I am looking forward to it. I think social skills are important, and especially when working with a team to understand and have clarity. I also think it would be cool to see how people think differently and that seems like a quick way to learn fast tips, etc.
3. How does pair programming work? There a Driver - the programmer. And a Navigator - keeps their focus on the big picture, while keeping an eye for bugs or typos.

## Node.js

> Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine.

### The V8 Engine

This is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers. It compiles JavaScript directly to native machine code, enabling high performance and efficient execution.

It's important to note that when we say "Node is built on the V8 engine", it does **not** mean that Node programs are executed in a browser. Rather, the creator of Node (Ryan Dahl) enhanced the V8 engine to run JavaScript on computers, thus creating a runtime environment.


### What is a Runtime?

A runtime environment is where programs execute and interact with the operating system and other software. In the context of Node.js, this means JavaScript can run outside a web browser, accessing resources like the file system, network, and much more.

### Install Node.js

There are a couple of options for installing Node.js:

1. Official Node Download Page: Go to Node.js Download to download the Node binaries for your system.

2. Version Manager: Alternatively, use a version manager, which allows you to install multiple versions of Node and switch between them. This is beneficial for handling different projects that may require specific Node versions, avoiding conflicts and dependency issues.

**Testing Your Installation:**

* To check your Node version, type `node -v` in your terminal.
* To verify npm's installation, type `npm -v`.

### npm, JavaScript Package Manager

npm, which comes bundled with Node.js, is the package manager for JavaScript. It is the world's largest software registry, offering a vast range of packages for various functionalities.

* **Functionality:** npm is not just for installing packages; it also manages dependencies and versions, making it easier to share and use code from the global developer community.
* **Largest Software Registry:** With npm, developers have access to over a million packages, streamlining the development process significantly.

### Practical Applications of Node.js

Node.js is widely used for developing backend services such as APIs, handling real-time data, and building server-side applications. Its non-blocking, event-driven architecture makes it particularly suited for applications that require real-time capabilities like chat applications, online gaming, and live streaming services.

