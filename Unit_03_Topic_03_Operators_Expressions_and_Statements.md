---
title: "Unit III: JavaScript Operators, Expressions, and Statements"
id: unit3-topic3-operators-expressions-statements
tags:
  - unit-3
  - javascript
  - operators
  - expressions
  - statements
  - control-flow
aliases:
  - "JS Operators"
  - "JS Control Flow"
links:
  - "[[UITx/Unit_03_Topic_02_Data_Types_and_Variables.md|Data Types and Variables]]"
  - "[[UITx/Unit_03_Topic_04_Functions_and_Scope.md|Functions and Scope]]"
---

# Unit III, Topic 3: JavaScript Operators, Expressions, and Statements

> [!quote] Just as words form sentences and sentences convey ideas, operators, expressions, and statements are the fundamental components that allow us to construct logical instructions in JavaScript. They are the grammar and vocabulary of programming, enabling us to manipulate data and control the flow of our applications. Let us now master this language.

## 1. JavaScript Operators

**Operators** are special symbols that perform operations on one or more values (operands) and produce a result.

### a) Assignment Operators
Assign a value to a variable.
-   `=` (assignment): `let x = 10;`
-   `+=`, `-=`, `*=`, `/=`, `%=`, `**=` (compound assignment): `x += 5;` (same as `x = x + 5;`)

### b) Arithmetic Operators
Perform mathematical calculations.
-   `+` (addition)
-   `-` (subtraction)
-   `*` (multiplication)
-   `/` (division)
-   `%` (modulus - remainder of division)
-   `**` (exponentiation - ES6+)
-   `++` (increment)
-   `--` (decrement)

**Example:**
```javascript
let a = 10;
let b = 3;
console.log(a + b); // 13
console.log(a % b); // 1
a++;
console.log(a);     // 11
```

### c) Comparison Operators
Compare two values and return a boolean (`true` or `false`).
-   `==` (loose equality): Compares values after type coercion.
-   `===` (strict equality): Compares values and types without type coercion. **(Always prefer this!)**
-   `!=` (loose inequality)
-   `!==` (strict inequality)
-   `>` (greater than)
-   `<` (less than)
-   `>=` (greater than or equal to)
-   `<=` (less than or equal to)

**Example:**
```javascript
console.log(5 == '5');   // true (type coercion)
console.log(5 === '5');  // false (strict comparison)
console.log(10 > 5);     // true
```

### d) Logical Operators
Combine boolean values and return a boolean.
-   `&&` (logical AND): Returns `true` if both operands are `true`.
-   `||` (logical OR): Returns `true` if at least one operand is `true`.
-   `!` (logical NOT): Inverts the boolean value of its operand.

**Example:**
```javascript
let isAdult = true;
let hasLicense = false;
console.log(isAdult && hasLicense); // false
console.log(isAdult || hasLicense); // true
console.log(!isAdult);              // false
```

### e) String Operators
-   `+` (concatenation): Joins two or more strings.
-   `+=` (compound assignment): `message += " World";`

**Example:**
```javascript
let hello = "Hello";
let world = " World";
console.log(hello + world); // "Hello World"
```

### f) Ternary (Conditional) Operator
A shorthand for an `if-else` statement.
-   `condition ? valueIfTrue : valueIfFalse;`

**Example:**
```javascript
let age = 18;
let status = (age >= 18) ? "Adult" : "Minor";
console.log(status); // "Adult"
```

## 2. Expressions

An **expression** is any valid unit of code that resolves to a value. Every expression can be evaluated to produce a single result.

**Examples of Expressions:**
-   `10` (a literal value)
-   `"Hello"` (a literal value)
-   `x` (a variable, evaluates to its value)
-   `a + b` (arithmetic expression, evaluates to a number)
-   `age >= 18` (comparison expression, evaluates to a boolean)
-   `myFunction()` (function call, evaluates to the function's return value)
-   `x = 10` (assignment expression, evaluates to 10)

## 3. Statements

A **statement** is a complete instruction that performs an action. Programs are made up of statements. Statements typically end with a semicolon (`;`), though it's often optional due to Automatic Semicolon Insertion (ASI), but it's good practice to include them.

**Examples of Statements:**
-   **Declaration Statement:** `let x = 10;`
-   **Assignment Statement:** `x = 20;`
-   **Control Flow Statements:**
    -   `if (condition) { /* ... */ } else { /* ... */ }`
    -   `for (let i = 0; i < 5; i++) { /* ... */ }`
    -   `while (condition) { /* ... */ }`
    -   `switch (value) { /* ... */ }`
-   **Function Declaration Statement:** `function greet() { /* ... */ }`
-   **Expression Statement:** An expression followed by a semicolon. `a + b;` (though this expression has no side effect, it's still a statement).

### Control Flow Statements

These statements control the order in which instructions are executed.

#### a) `if...else if...else`
Executes different blocks of code based on conditions.

```javascript
let score = 85;
if (score >= 90) {
    console.log("Grade A");
} else if (score >= 80) {
    console.log("Grade B");
} else {
    console.log("Grade C");
}
```

#### b) `switch`
Executes different blocks of code based on different cases of a single variable.

```javascript
let day = "Monday";
switch (day) {
    case "Monday":
        console.log("Start of the week.");
        break;
    case "Friday":
        console.log("End of the week.");
        break;
    default:
        console.log("Mid-week.");
}
```

#### c) `for` Loop
Repeats a block of code a specific number of times.

```javascript
for (let i = 0; i < 3; i++) {
    console.log("Loop iteration: " + i);
}
```

#### d) `while` Loop
Repeats a block of code as long as a specified condition is true.

```javascript
let count = 0;
while (count < 3) {
    console.log("Count: " + count);
    count++;
}
```

#### e) `do...while` Loop
Similar to `while`, but the block of code is executed at least once before the condition is tested.

```javascript
let i = 0;
do {
    console.log("Do-while count: " + i);
    i++;
} while (i < 0); // Condition is false, but loop runs once
```

## 4. Exam-Oriented Insights

Operators, expressions, and statements are the bedrock of programming logic.

> [!question] **Potential 2-Mark Questions:**
> 1.  **Differentiate between `==` and `===` operators in JavaScript.**
>     *Answer:* `==` (loose equality) compares values after performing type coercion, while `===` (strict equality) compares both values and their types without any type conversion.
> 2.  **What is the purpose of the `&&` operator?**
>     *Answer:* The `&&` (logical AND) operator returns `true` if both of its operands are `true`; otherwise, it returns `false`.
> 3.  **Give an example of an expression in JavaScript.**
>     *Answer:* `10 + 5`, `"Hello" + name`, `age >= 18`, `myFunction()` (any valid code that resolves to a value).
> 4.  **Name two control flow statements in JavaScript.**
>     *Answer:* `if...else`, `for` loop, `while` loop, `switch` (any two).

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a short JavaScript code snippet that uses a combination of different operators and control flow statements to solve a simple problem (e.g., calculate a grade based on a score, iterate through an array). Explain the concept of operator precedence and associativity. Discuss the importance of using strict equality (`===`) to avoid common pitfalls related to type coercion.
