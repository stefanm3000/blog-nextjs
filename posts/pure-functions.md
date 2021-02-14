---
title: "Explain pure functions + coding example"
date: "2021-02-14"
---

A pure function is a function which:
- Given the same input, will always return the same output.
- Produces no side effects.

A dead giveaway that a function is impure is if it makes sense to call it without using its return value.

Pure functions take some input and return some output based on that input. They are the simplest reusable building blocks of code in a program. Perhaps the most important design principle in computer science is KISS (Keep It Simple, Stupid). 

A function is only pure if, given the same input, it will always produce the same output. You may remember this rule from algebra class: the same input values will always map to the same output value. However, many input values may map to the same output value. 

**pure**: 

const add = (x, y) => x + y;

add(2, 4); // 6

**impure**:

let x = 2;        // affects the output

const add = (y) => {
  x += y;
};

add(4); // x === 6 (the first time)

