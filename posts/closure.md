---
title: "What is closure? Coding example? What are the advantages of using closure in your code?"
date: "2021-02-14"
---

A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

**Coding example:**

    const newFunc = () => {
        const x = 1;
        const scopedFunc = () => {
             return x + 1;
            };
        return scopedFunc();
    };

newFunc();
