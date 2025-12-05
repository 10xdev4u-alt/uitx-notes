---
title: "Unit III: Introduction to JavaScript and Core Features"
id: unit3-topic1-intro-javascript
tags:
  - unit-3
  - javascript
  - programming
  - web-development
  - client-side
aliases:
  - "What is JavaScript"
  - "JS Core Features"
links:
  - "[[UITx/Unit_02_Quiz.md|Unit 02 Quiz]]"
  - "[[UITx/Unit_03_Topic_02_Data_Types_and_Variables.md|Data Types and Variables]]"
---

# Unit III, Topic 1: Introduction to JavaScript and Core Features

> [!quote] If HTML provides the structure and CSS the style, then JavaScript breathes life into the web page, transforming it from a static document into a dynamic, interactive experience. It is the language of interactivity, enabling complex behaviors and real-time updates. Let us now embark on the journey to master this essential web technology.

## 1. What is JavaScript?

**JavaScript (JS)** is a high-level, often just-in-time compiled, and multi-paradigm programming language. It is best known as the scripting language for web pages, but it's used in many non-browser environments as well (e.g., Node.js for server-side, Electron for desktop apps, React Native for mobile apps).

### Key Roles in Web Development:
-   **Client-Side Scripting:** Primarily, JavaScript runs in the user's web browser, allowing developers to create dynamic and interactive web pages. This includes:
    -   Manipulating HTML content and CSS styles.
    -   Responding to user actions (clicks, key presses, mouse movements).
    -   Validating form input before submission.
    -   Making asynchronous requests to a server (AJAX).
    -   Creating animations and interactive elements.
-   **Server-Side Scripting (Node.js):** With Node.js, JavaScript can also be used to build scalable network applications, including web servers and APIs.

## 2. A Brief History of JavaScript

-   **1995:** Created by Brendan Eich at Netscape Communications under the name "Mocha," later renamed to "LiveScript," and finally "JavaScript." It was initially designed to add interactivity to web pages.
-   **1996:** Microsoft released JScript, a reverse-engineered version of JavaScript, for Internet Explorer.
-   **1997:** JavaScript was submitted to ECMA International for standardization, resulting in **ECMAScript**. ECMAScript is the standard, and JavaScript is the most popular implementation of that standard.
-   **Evolution:** JavaScript has continuously evolved, with new versions of ECMAScript (ES6/ES2015, ES2016, etc.) introducing significant new features and syntax improvements.

## 3. Core Features of JavaScript

### a) High-Level Language
-   Abstracts away many complexities of computer architecture, allowing developers to focus on logic rather than memory management.

### b) Interpreted (or Just-in-Time Compiled)
-   Traditionally, JavaScript was an interpreted language. Modern JavaScript engines (like V8 in Chrome) use Just-in-Time (JIT) compilation, which compiles JavaScript code into machine code at runtime for better performance.

### c) Multi-Paradigm
-   Supports various programming styles:
    -   **Object-Oriented Programming (OOP):** Through prototypes and, more recently, classes.
    -   **Imperative Programming:** Focuses on *how* a program operates.
    -   **Declarative Programming:** Focuses on *what* the program should accomplish.
    -   **Functional Programming:** Treats computation as the evaluation of mathematical functions.

### d) Dynamically Typed
-   Variables in JavaScript are not declared with a specific type (e.g., `int`, `string`). The type of a variable is determined at runtime based on the value it holds.
-   **Example:**
    ```javascript
    let x = 10;       // x is a number
    x = "hello";      // x is now a string
    ```

### e) Event-Driven
-   JavaScript is highly responsive to events (user clicks, page loads, key presses, etc.). This is fundamental to creating interactive user interfaces.

### f) Prototype-Based Object-Oriented
-   Unlike class-based OOP languages (like Java or C++), JavaScript uses prototypes for inheritance. Objects can inherit properties and methods directly from other objects. (ES6 introduced `class` syntax, which is syntactic sugar over prototypes).

### g) First-Class Functions
-   Functions are treated as regular variables. They can be assigned to variables, passed as arguments to other functions, and returned from functions. This enables powerful patterns like callbacks and higher-order functions.

## 4. Including JavaScript in HTML

There are three main ways to include JavaScript in an HTML document:

### a) Inline JavaScript (Avoid for best practice)
-   Directly within HTML tags using event attributes.
-   **Use sparingly** as it mixes content and behavior, making code harder to maintain.
    ```html
    <button onclick="alert('Hello!');">Click me</button>
    ```

### b) Internal JavaScript
-   Placed within `<script>` tags in the `<head>` or `<body>` section of the HTML document.
-   Good for small, page-specific scripts.
    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Internal JS</title>
        <script>
            function greet() {
                alert('Hello from internal script!');
            }
        </script>
    </head>
    <body>
        <button onclick="greet()">Greet</button>
    </body>
    </html>
    ```

### c) External JavaScript (Recommended)
-   Placed in separate `.js` files and linked to the HTML document using the `<script src="path/to/script.js"></script>` tag.
-   **Best practice** for larger projects as it promotes code organization, reusability, and caching.
    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>External JS</title>
    </head>
    <body>
        <button id="myButton">Click me</button>
        <script src="my_script.js"></script>
    </body>
    </html>
    ```
    **`my_script.js`:**
    ```javascript
    document.getElementById('myButton').addEventListener('click', function() {
        alert('Hello from external script!');
    });
    ```
-   **`defer` attribute:** If placed in the `<head>`, `defer` ensures the script executes after the HTML is parsed, but before the `DOMContentLoaded` event.
-   **`async` attribute:** If placed in the `<head>`, `async` downloads the script asynchronously and executes it as soon as it's downloaded, potentially before HTML parsing is complete.

## 5. Exam-Oriented Insights

JavaScript is a cornerstone of web development.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the primary role of JavaScript in web development?**
>     *Answer:* JavaScript is primarily used for client-side scripting to create dynamic and interactive web pages, responding to user actions and manipulating page content.
> 2.  **Differentiate between JavaScript and ECMAScript.**
>     *Answer:* ECMAScript is the standardized specification for a general-purpose scripting language, while JavaScript is the most popular implementation of that standard, primarily used for web browsers.
> 3.  **List two core features of JavaScript.**
>     *Answer:* High-level, dynamically typed, multi-paradigm, event-driven, prototype-based object-oriented, first-class functions (any two).
> 4.  **What is the recommended way to include JavaScript in an HTML document for larger projects, and why?**
>     *Answer:* External JavaScript files (`<script src="...">`) are recommended because they promote code organization, reusability, and allow browsers to cache the script, improving page load times.

> [!tip] **For Higher Mark Questions:**
> Be prepared to explain the evolution of JavaScript and its relationship with ECMAScript. Discuss the advantages and disadvantages of client-side vs. server-side JavaScript. Provide a simple HTML document with an external JavaScript file that demonstrates a basic interactive element (e.g., changing text on a button click). Explain the concepts of dynamic typing and event-driven programming with examples.
