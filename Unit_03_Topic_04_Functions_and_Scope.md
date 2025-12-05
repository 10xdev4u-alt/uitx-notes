---
title: "Unit III: JavaScript Functions and Scope"
id: unit3-topic4-functions-scope
tags:
  - unit-3
  - javascript
  - functions
  - scope
  - closure
  - hoisting
aliases:
  - "JS Functions"
  - "JS Scope"
links:
  - "[[UITx/Unit_03_Topic_03_Operators_Expressions_and_Statements.md|Operators, Expressions and Statements]]"
  - "[[UITx/Unit_03_Topic_05_Objects.md|Objects]]"
---

# Unit III, Topic 4: JavaScript Functions and Scope

> [!quote] Functions are the verbs of programming, encapsulating actions and logic into reusable blocks. Scope defines the boundaries within which our variables and functions are visible and accessible. Together, they form the backbone of organized and modular JavaScript code. Let us now master these pillars of code structure.

## 1. JavaScript Functions

A **function** is a block of code designed to perform a particular task. Functions are executed when "something" invokes or calls them.

### a) Function Declaration
The traditional way to define a function. These are hoisted, meaning you can call them before they are declared in the code.

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("Alice")); // Output: Hello, Alice!
```

### b) Function Expression
A function defined as part of an expression. These are not hoisted in the same way; you cannot call them before they are defined.

```javascript
const sayHello = function(name) {
    return `Hello, ${name}!`;
};
console.log(sayHello("Bob")); // Output: Hello, Bob!
```

### c) Arrow Functions (ES6+)
A more concise syntax for writing function expressions, especially useful for short, single-line functions. They also have different behavior regarding `this` (which we'll cover later).

```javascript
const multiply = (a, b) => a * b;
console.log(multiply(5, 3)); // Output: 15

const sayHi = () => console.log("Hi!");
sayHi(); // Output: Hi!
```

### d) Function Parameters and Arguments
-   **Parameters:** The names listed in the function definition (e.g., `name` in `greet(name)`).
-   **Arguments:** The real values passed to the function when it is called (e.g., `"Alice"` in `greet("Alice")`).

### e) Return Values
Functions can return a value using the `return` statement. If no `return` statement is specified, the function implicitly returns `undefined`.

## 2. Scope in JavaScript

**Scope** determines the accessibility (visibility) of variables, objects, and functions in different parts of your code.

### a) Global Scope
-   Variables declared outside any function or block are in the global scope.
-   They are accessible from anywhere in the code (inside functions, blocks, etc.).
-   **Avoid polluting the global scope** as it can lead to naming conflicts and make code harder to manage.

```javascript
let globalVar = "I am global";

function accessGlobal() {
    console.log(globalVar); // Accessible
}
accessGlobal();
```

### b) Function Scope (or Local Scope)
-   Variables declared inside a function (using `var`, `let`, or `const`) are function-scoped.
-   They are only accessible from within that function.

```javascript
function localScopeExample() {
    let localVar = "I am local to this function";
    console.log(localVar);
}
localScopeExample();
// console.log(localVar); // ReferenceError: localVar is not defined
```

### c) Block Scope (ES6+ with `let` and `const`)
-   Variables declared with `let` or `const` inside a block (any code enclosed in `{}`) are block-scoped.
-   They are only accessible within that specific block.

```javascript
if (true) {
    let blockVar = "I am block-scoped";
    console.log(blockVar);
}
// console.log(blockVar); // ReferenceError: blockVar is not defined

for (let i = 0; i < 1; i++) {
    const loopVar = "I am also block-scoped";
    console.log(loopVar);
}
// console.log(loopVar); // ReferenceError: loopVar is not defined
```

### d) Lexical Scope (Static Scope)
-   JavaScript uses lexical scoping, meaning the scope of a variable is determined by its position in the source code when it is written, not when it is called.
-   Inner functions have access to variables of their outer (parent) functions.

```javascript
function outer() {
    let outerVar = "I am from outer";
    function inner() {
        console.log(outerVar); // inner function can access outerVar
    }
    inner();
}
outer(); // Output: I am from outer
```

## 3. Closures

A **closure** is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In simpler terms, a closure gives you access to an outer function's scope from an inner function, even after the outer function has finished executing.

This is a powerful concept for creating private variables and maintaining state.

**Example:**
```javascript
function makeCounter() {
    let count = 0; // 'count' is in the lexical environment of makeCounter
    return function() { // This inner function is the closure
        count++;
        return count;
    };
}

const counter1 = makeCounter();
console.log(counter1()); // Output: 1
console.log(counter1()); // Output: 2

const counter2 = makeCounter(); // Creates a new, independent lexical environment
console.log(counter2()); // Output: 1
```
Here, `counter1` and `counter2` are closures. They both "remember" their own `count` variable from their respective calls to `makeCounter()`.

## 4. Hoisting

**Hoisting** is a JavaScript mechanism where variable and function declarations are moved to the top of their containing scope during the compilation phase, *before* code execution.

-   **`var` declarations:** Are hoisted and initialized with `undefined`.
-   **`let` and `const` declarations:** Are hoisted but *not* initialized. They are in a "temporal dead zone" until their actual declaration in the code.
-   **Function declarations:** Are fully hoisted, meaning you can call them before their definition.
-   **Function expressions (including arrow functions):** Are treated like variable declarations and only their declaration is hoisted (not their assignment).

**Example:**
```javascript
console.log(hoistedVar);   // undefined (var is hoisted and initialized)
var hoistedVar = "I am hoisted var";

// console.log(hoistedLet); // ReferenceError: Cannot access 'hoistedLet' before initialization
let hoistedLet = "I am hoisted let";

hoistedFunction(); // Output: I am a hoisted function!
function hoistedFunction() {
    console.log("I am a hoisted function!");
}

// notHoistedFunction(); // TypeError: notHoistedFunction is not a function
const notHoistedFunction = function() {
    console.log("I am not hoisted!";
};
```

## 5. Exam-Oriented Insights

Functions and scope are critical for writing structured and bug-free JavaScript.

> [!question] **Potential 2-Mark Questions:**
> 1.  **Differentiate between a function declaration and a function expression.**
>     *Answer:* Function declarations are hoisted and can be called before their definition, while function expressions are not fully hoisted and must be defined before they are called.
> 2.  **What is the primary difference between global scope and function scope?**
>     *Answer:* Global scope variables are accessible from anywhere in the code, whereas function-scoped variables are only accessible within the function where they are declared.
> 3.  **Explain the concept of a closure in JavaScript.**
>     *Answer:* A closure is an inner function that retains access to the variables of its outer (enclosing) function's scope, even after the outer function has finished executing.
> 4.  **What is hoisting in JavaScript?**
>     *Answer:* Hoisting is a JavaScript mechanism where variable and function declarations are moved to the top of their containing scope during the compilation phase, before code execution.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write code examples demonstrating global, function, and block scope, explaining the visibility of variables in each. Provide an example of a closure and explain how it allows for data privacy or state management. Discuss the nuances of hoisting for `var`, `let`, `const`, and function declarations vs. expressions, highlighting potential pitfalls.
