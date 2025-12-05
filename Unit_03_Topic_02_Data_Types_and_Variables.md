---
title: "Unit III: JavaScript Data Types and Variables"
id: unit3-topic2-data-types-variables
tags:
  - unit-3
  - javascript
  - data-types
  - variables
  - let
  - const
  - var
aliases:
  - "JS Data Types"
  - "JS Variables"
links:
  - "[[UITx/Unit_03_Topic_01_Intro_to_JavaScript_and_Core_Features.md|Introduction to JavaScript and Core Features]]"
  - "[[UITx/Unit_03_Topic_03_Operators_Expressions_and_Statements.md|Operators, Expressions and Statements]]"
---

# Unit III, Topic 2: JavaScript Data Types and Variables

> [!quote] In the realm of programming, data is the essence, and variables are the vessels that hold this essence. Understanding how JavaScript categorizes and stores information is fundamental to writing effective and predictable code. Let us now explore the basic building blocks of JavaScript data.

## 1. What are Variables?

A **variable** is a named storage location for data. Think of it as a labeled box where you can put different kinds of information. In JavaScript, you declare variables using keywords like `var`, `let`, or `const`.

### a) `var` (Legacy)
-   Introduced in early JavaScript.
-   **Function-scoped:** Variables declared with `var` are accessible throughout the function they are declared in, regardless of block scope (e.g., `if` statements, `for` loops).
-   **Hoisted:** Declarations are "hoisted" to the top of their function or global scope, meaning you can use a `var` variable before it's declared (though it will be `undefined`).
-   **Can be re-declared and re-assigned:** This can lead to unexpected behavior and bugs.

**Example:**
```javascript
function exampleVar() {
    console.log(x); // undefined (hoisted)
    var x = 10;
    if (true) {
        var x = 20; // Re-declares x within the same function scope
        console.log(x); // 20
    }
    console.log(x); // 20 (x is function-scoped)
}
exampleVar();
// console.log(x); // ReferenceError: x is not defined (x is not global)
```

### b) `let` (Modern, ES6+)
-   Introduced in ECMAScript 2015 (ES6) to address issues with `var`.
-   **Block-scoped:** Variables declared with `let` are only accessible within the block (e.g., `if` statement, `for` loop, function) where they are defined.
-   **Not hoisted (or "temporally dead zone"):** While `let` declarations are technically hoisted, they are not initialized. Accessing a `let` variable before its declaration results in a `ReferenceError`.
-   **Can be re-assigned, but not re-declared:** You can change its value, but you cannot declare another `let` variable with the same name in the same scope.

**Example:**
```javascript
function exampleLet() {
    // console.log(y); // ReferenceError: Cannot access 'y' before initialization
    let y = 10;
    if (true) {
        let y = 20; // Declares a new 'y' in block scope
        console.log(y); // 20
    }
    console.log(y); // 10 (y is block-scoped)
}
exampleLet();
```

### c) `const` (Modern, ES6+)
-   Introduced in ES6.
-   **Block-scoped:** Similar to `let`.
-   **Not hoisted (temporally dead zone):** Similar to `let`.
-   **Cannot be re-assigned or re-declared:** Once a `const` variable is assigned a value, it cannot be changed. It must be initialized at the time of declaration.
-   **Important Note:** For objects and arrays, `const` prevents re-assignment of the variable itself, but it *does not* prevent modification of the object's properties or array's elements.

**Example:**
```javascript
const PI = 3.14159;
// PI = 3.14; // TypeError: Assignment to constant variable.

const user = { name: "Alice" };
user.name = "Bob"; // This is allowed!
// user = { name: "Charlie" }; // TypeError: Assignment to constant variable.
```

> [!tip] **Best Practice:**
> Always prefer `const` when the variable's value will not change. If the value needs to change, use `let`. Avoid `var` in modern JavaScript development.

## 2. JavaScript Data Types

JavaScript is a dynamically typed language, meaning you don't explicitly declare the type of a variable. The type is determined by the value it holds. JavaScript has seven primitive data types and one complex data type.

### Primitive Data Types:

1.  **`string`**: Represents textual data. Enclosed in single quotes (`' '`), double quotes (`" "`), or backticks (`` ` `` for template literals).
    ```javascript
    let name = "John Doe";
    let greeting = 'Hello';
    let message = `Welcome, ${name}!`; // Template literal
    ```

2.  **`number`**: Represents both integer and floating-point numbers.
    ```javascript
    let age = 30;
    let price = 99.99;
    let bigNumber = 123e5; // 12300000
    ```

3.  **`boolean`**: Represents a logical entity and can have two values: `true` or `false`.
    ```javascript
    let isActive = true;
    let hasPermission = false;
    ```

4.  **`undefined`**: Represents a variable that has been declared but has not yet been assigned a value.
    ```javascript
    let city;
    console.log(city); // undefined
    ```

5.  **`null`**: Represents the intentional absence of any object value. It is a primitive value.
    ```javascript
    let car = null;
    console.log(typeof null); // "object" - This is a long-standing bug in JavaScript.
    ```

6.  **`symbol`** (ES6+): Represents a unique identifier. Used for creating unique object property keys.
    ```javascript
    const id = Symbol('id');
    const anotherId = Symbol('id');
    console.log(id === anotherId); // false
    ```

7.  **`bigint`** (ES2020+): Represents whole numbers larger than `2^53 - 1`, which is the largest number JavaScript can reliably represent with the `number` type.
    ```javascript
    const largeNum = 9007199254740991n; // 'n' at the end makes it a BigInt
    ```

### Complex Data Type:

1.  **`object`**: Represents a collection of properties, where each property has a name (or key) and a value. Objects are the most fundamental complex data type.
    -   **Plain Objects:**
        ```javascript
        let person = {
            firstName: "Jane",
            lastName: "Doe",
            age: 25
        };
        ```
    -   **Arrays:** Special type of object for ordered collections of data.
        ```javascript
        let colors = ["red", "green", "blue"];
        ```
    -   **Functions:** Functions are also objects in JavaScript.
        ```javascript
        function greet() { /* ... */ }
        ```
    -   **Date, Math, RegExp, etc.:** Built-in objects.

### Checking Data Types: `typeof` Operator

The `typeof` operator returns a string indicating the type of the unevaluated operand.

```javascript
console.log(typeof "hello");      // "string"
console.log(typeof 123);          // "number"
console.log(typeof true);         // "boolean"
console.log(typeof undefined);    // "undefined"
console.log(typeof null);         // "object" (historical bug)
console.log(typeof Symbol('id')); // "symbol"
console.log(typeof 10n);          // "bigint"
console.log(typeof {});           // "object"
console.log(typeof []);           // "object"
console.log(typeof function(){}); // "function" (special case of object)
```

## 3. Type Coercion

JavaScript is loosely typed, which means it performs **type coercion** (automatic type conversion) when operations involve values of different types. This can sometimes lead to unexpected results.

**Example:**
```javascript
console.log(10 + "5");   // "105" (number 10 is coerced to string "10")
console.log(10 - "5");   // 5   (string "5" is coerced to number 5)
console.log(true + 1);   // 2   (true is coerced to 1)
console.log("5" == 5);   // true (loose equality, type coercion happens)
console.log("5" === 5);  // false (strict equality, no type coercion)
```
> [!tip] **Strict Equality (`===`)**
> Always prefer the strict equality operator (`===`) over the loose equality operator (`==`) to avoid unexpected type coercion issues.

## 4. Exam-Oriented Insights

Understanding data types and variables is foundational for JavaScript.

> [!question] **Potential 2-Mark Questions:**
> 1.  **Differentiate between `var` and `let` in JavaScript.**
>     *Answer:* `var` is function-scoped and hoisted, while `let` is block-scoped and not initialized before declaration (temporal dead zone). `var` can be re-declared, `let` cannot.
> 2.  **What is the purpose of the `const` keyword, and what is a key limitation when used with objects?**
>     *Answer:* `const` declares a block-scoped, read-only named constant that cannot be re-assigned. For objects, `const` prevents re-assignment of the variable itself, but it *does not* prevent modification of the object's properties.
> 3.  **List three primitive data types in JavaScript.**
>     *Answer:* `string`, `number`, `boolean`, `undefined`, `null`, `symbol`, `bigint` (any three).
> 4.  **What is type coercion in JavaScript, and why can it be problematic?**
>     *Answer:* Type coercion is JavaScript's automatic conversion of values from one data type to another when operations involve different types. It can be problematic because it can lead to unexpected results and bugs if not understood.

> [!tip] **For Higher Mark Questions:**
> Be prepared to explain the differences between `var`, `let`, and `const` in detail, including scope and hoisting, with code examples illustrating their behavior. Discuss the concept of dynamic typing and type coercion, providing examples of how `==` and `===` behave differently. Explain why `typeof null` returns "object" and its historical context.
