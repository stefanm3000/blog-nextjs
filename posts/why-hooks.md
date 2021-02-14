---
title: "React hooks with coding example"
date: "2021-02-14"
---

A **great** [codesandbox page](https://codesandbox.io/s/github/btholt/react-hooks-examples/tree/master/) which showcases most of the hooks available in React.

Basically, about 99% of use cases can be covered with useState, useEffect, useContext and useRef.

- **useState**: useState allows us to make our components stateful. Whereas this previously required using a class component, hooks give us the ability to write it using just functions. It allows us to have more flexible components. In our example component, everytime you click on the h1 (bad a11y, by the way) it'll change colors. It's doing this by keeping that bit of state in a hook which is being fed in anew every render so it always has the latest state.

- **useEffect**: Effects are how you recreate componentDidMount, componentDidUpdate, and componentDidUnmount from React. Inside useEffect, you can do any sort of side-effect type action that you would have previously done in one of React's lifecycle methods. You can do things like fire AJAX requests, integrate with third party libraries (like a jQuery plugin), fire off some telemetry, or anything else that needs to happen on the side for your component.

- **useContext**: An early problem with the React problem is called "data tunneling" or "prop drilling". This is when you have a top level component (in our case the parent component) and a child component way down in the hierarchy that need the same data (like the user object.) We could pass that data down, parent-to-child, for each of the intermediary components but that sucks because now each of LevelTwo, LevelThree, and LevelFour all have to know about the user object even when they themselves don't need it, just their children. This is prop drilling: passing down this data in unnecessary intermediaries.

- **useRef**: Refs are useful for several things, we'll explore two of the main reasons in these examples. I want to show you the first use case: how to emulate instance variables from React.

    In order to understand why refs are useful, you need to understand how closures work. In our component, when a user clicks, it sets a timeout to log both the state and the ref's number after a second. One thing to keep in mind that the state and the ref's number are always the same. They are never out of lockstep since they're updated at the same time. However, since we delay the logging for a second, when it alerts the new values, it will capture what the state was when we first called the timeout (since it's held on to by the closure) but it will always log the current value since that ref is on an object that React consistently gives the same object back to you. Because it's the same object and the number is a property on the object, it will always be up to date and not subject to the closure's scope.
