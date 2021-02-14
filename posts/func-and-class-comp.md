---
title: "Diff between functional and class components in react?"
date: "2021-02-14"
---

**Functional Component**: 

- It is simple javascript functions that simply returns html UI

- It is also called “stateless” components because they simply accept data and display them in some form that is they are mainly responsible for rendering UI.

- It accept properties(props) in function and return html(JSX)

- It gives solution without using state

- There is no render method used in functional components.

- These can be typically defined using arrow functions but can also be created with the regular function keyword.

- We can use React Hooks in functional component, useEffect() hook can be used to replicate lifecycle behaviour, and useState can be used to store state in a functional component.


**Class Component**: 

- Class Component or Stateful Component

- It is regular ES6 classes that extends component class form react library

- Also known as “stateful” components because they implement logic and state.

- It must have render() method returning html

- It has complex UI Logic

- You pass props to class components and access them with this.props

- Lifecycle methods such as componentDidMount, componentDidUpdate etc are harder to read and write