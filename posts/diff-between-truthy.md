---
title: "Difference between == and === ?"
date: "2021-02-14"
---

JavaScript likes to convert values to other types implicitly whenever possible. Because of that, when comparing booleans to other types of variables, JavaScript uses the same logic as older programming languages. A value that represents empty, null, or zero (such as 0, or "") evaluates to false, and any other value (such as 1, 5, -19, "ghsfsah", or other meaningful content) evaluates to true.

Why does it do this? Well for one it allows developers a small shortcut when checking to see if a variable has content. For example, if a user doesn't give input in a text field, we can easily check to see if a field is empty and prompt the user.

**Equality ( == ):**

console.log(1 == 1);
// expected output: true

console.log('hello' == 'hello');
// expected output: true

console.log('1' == 1);
// expected output: true

console.log(0 == false);
// expected output: true

**Strict equality ( === ):**

console.log(1 === 1);
// expected output: true

console.log('hello' === 'hello');
// expected output: true

console.log('1' === 1);
// expected output: false

console.log(0 === false);
// expected output: false
