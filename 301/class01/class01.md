[[301/README|Module 301]]
# Introduction to React and Components

Reading assignment for Class 01

## Questions & Answers

[Component-Based Architecture](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

1. What is a "component"? A component is jsx file that can have simple or complex functions.
2. What are the characteristics of a component? Components can be reused, replaced, extendable, and independent.
3. What are the advantages of using component-based architecture? Increases reliability and reduced development resources of time and money.

[What is Props and How to Use in React](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0)

1. What is "props" short for? Properties
2. How are props used in React? They are used to share data from one component to the next.
3. What is the flow of props? Uni-directional flow from Parent to child.

## Component-Based Architecture

>Component-based architecture focuses on the decomposition of the design into individual functional or logical components that represent well-defined communication interfaces containing methods, events, and properties. It provides a higher level of abstraction and divides the problem into sub-problems, each associated with component partitions.

Basically a way that breaks down an application into smaller puzzle pieces called components.

Advantages:

* Reduced time in development with reusing existing components.
* Increased reliability with reuse of existing components

### What is a Component?

>A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

#### Views of a Component

* Object-oriented view
* Conventional view
* Process-related view

#### Characteristics of Components

* Reusability - Can be used in various situations in different applications
* Replaceable - Freely substituted with similar components
* Not context specific - Designed to operate in varying environments
* Extensible - Can be extended (connected) from existing components to provide new behavior
* Encapsulated - Depicts the interfaces which allows to use to use its functions, but does not expose details of internal processes, variables, or state
* Independent - Designed to have minimal dependencies on other components

## What is "Props" and how to use it in React?

### What is Props?

"Props" - Keyword in React that stands for **Properties.** It is used for passing data from one component to another.

It is passed in a **uni-directional flow.** Meaning it is one way from parent to child.

It is also **data read-only**, as in the data coming from the parent **should not** be changed by the child component.
