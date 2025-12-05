---
title: "Unit III Quiz: JavaScript and XML"
id: unit3-quiz
tags:
  - unit-3
  - quiz
  - assessment
  - javascript
  - dom
  - json
  - ajax
aliases:
  - "Unit 3 Assessment"
links:
  - "[[UITx/Unit_03_Topic_13_Intro_to_XML_and_AJAX.md|Introduction to XML and AJAX]]"
---

# Unit III Quiz: JavaScript and XML

> [!note] This quiz is designed to test your understanding of the core concepts of JavaScript covered in Unit III, from its fundamental syntax to DOM manipulation, OOP techniques, and data interchange formats like JSON and XML.

## Section 1: Quiz Questions (Multiple Choice / Short Answer)

1.  Which keyword is used to declare a block-scoped variable that can be reassigned?
    a) `var`
    b) `const`
    c) `let`
    d) `static`
2.  What is the output of `typeof null` in JavaScript?
3.  Which built-in JavaScript object is used for working with dates and times?
4.  What is the DOM?
    a) A JavaScript framework
    b) A server-side language
    c) A programming interface for HTML documents
    d) A data-interchange format
5.  Which method is the modern, recommended way to attach an event handler to an element?
6.  The top-level object in the Browser Object Model (BOM) is the ______ object.
7.  To prevent a form from submitting normally when the submit button is clicked, you would call which method on the event object?
8.  In JavaScript, what is the primary difference between `==` and `===`?
9.  Which built-in JavaScript object is used to convert a JavaScript object into a JSON string?
10. What does AJAX stand for?

## Section 2: Reasoning Questions

1.  Explain the difference between `var`, `let`, and `const` in terms of scope and re-assignability. Why is it recommended to avoid `var` in modern JavaScript?
2.  What is a closure in JavaScript? Provide a simple code example and explain how it works.
3.  Describe the difference between the DOM and the BOM. Give one example of an object from each.
4.  Explain the concept of event bubbling. How can you stop it?
5.  What is the prototype chain and how does it enable inheritance in JavaScript?
6.  Why is it necessary to use `JSON.stringify()` before storing a JavaScript object in `localStorage`?
7.  Compare and contrast JSON and XML as data interchange formats, mentioning at least two differences.
8.  Explain the purpose of the `this` keyword and how its value can change depending on how a function is called (e.g., as a method vs. a standalone function).
9.  What is the difference between `innerHTML` and `textContent` when manipulating DOM elements? When would you prefer one over the other?
10. Describe the asynchronous nature of an AJAX request using `XMLHttpRequest`. What is the role of the `onload` or `onreadystatechange` event handler?

## Section 3: Real-World Cases

1.  **Case: A "Dark Mode" Toggle**
    You want to create a "dark mode" toggle button on a website. When the user clicks it, the theme should change. If the user closes and reopens their browser, their theme preference should be remembered. Which Web Storage object (`localStorage` or `sessionStorage`) would you use and why?
2.  **Case: Interactive To-Do List**
    You are building a to-do list. When a user clicks on a list item, you want to draw a line through it by adding a CSS class named `completed`. Which DOM event would you listen for, and how would you implement this functionality?
3.  **Case: Form Validation**
    A user registration form has a "password" field and a "confirm password" field. You need to write JavaScript to check if the values in both fields match before the form is submitted. Which event would you use to trigger this validation, and what would you do if the passwords don't match?
4.  **Case: A Countdown Timer**
    You need to display a countdown timer on a webpage that updates every second. Which method on the `window` object would be most appropriate for this task?
5.  **Case: Dynamic Content Loading**
    A blog's homepage shows the 10 most recent posts. At the bottom, there is a "Load More" button. When clicked, it should fetch the next 10 posts from the server without reloading the entire page. What technology is used for this, and what data format would be ideal for the server to send back?
6.  **Case: Creating Multiple User Objects**
    You are building an application that needs to create many `User` objects, each with a `name` and an `email` property, and a `login()` method. Would you use a simple object literal for each user, or would a `class` (or constructor function) be more appropriate? Why?
7.  **Case: Accessing Nested Data**
    You receive the following JSON string from an API: `'{"id": 1, "data": {"status": "active"}}'`. Write the JavaScript code to parse this string and access the value of the `status` property.
8.  **Case: A Simple Calculator**
    You are building a simple calculator UI. Which JavaScript built-in object would you use to perform operations like finding the square root or rounding a number?
9.  **Case: Navigating Browser History**
    Your web application has a custom "Back" button. How would you use the BOM to make this button behave exactly like the browser's native back button?
10. **Case: A "Hoisting" Pitfall**
    A developer writes `console.log(myVar);` at the top of their script, and `var myVar = 10;` at the bottom. What is logged to the console and why?

## Section 4: Rapid Fire Questions

1.  What keyword is used to declare a constant variable?
2.  Which operator checks for both value and type equality?
3.  What is the output of `10 + "5"`?
4.  Which array method adds an element to the end of an array?
5.  What is the index of the first element in an array?
6.  Which method is used to select the first element that matches a CSS selector?
7.  What event is fired when a user clicks an element?
8.  Which object in the BOM contains information about the current URL?
9.  What does `JSON.parse()` do?
10. What is the modern, promise-based alternative to `XMLHttpRequest`?

## Section 5: All Possible 2-Mark Remember Questions

*From Unit III, Topic 1: Introduction to JavaScript and Core Features*
1.  What is the primary role of JavaScript in web development?
2.  Differentiate between JavaScript and ECMAScript.
3.  List two core features of JavaScript.
4.  What is the recommended way to include JavaScript in an HTML document for larger projects, and why?

*From Unit III, Topic 2: JavaScript Data Types and Variables*
5.  Differentiate between `var` and `let` in JavaScript.
6.  What is the purpose of the `const` keyword, and what is a key limitation when used with objects?
7.  List three primitive data types in JavaScript.
8.  What is type coercion in JavaScript, and why can it be problematic?

*From Unit III, Topic 3: JavaScript Operators, Expressions, and Statements*
9.  Differentiate between `==` and `===` operators in JavaScript.
10. What is the purpose of the `&&` operator?
11. Give an example of an expression in JavaScript.
12. Name two control flow statements in JavaScript.

*From Unit III, Topic 4: JavaScript Functions and Scope*
13. Differentiate between a function declaration and a function expression.
14. What is the primary difference between global scope and function scope?
15. Explain the concept of a closure in JavaScript.
16. What is hoisting in JavaScript?

*From Unit III, Topic 5: JavaScript Objects*
17. What is a JavaScript object?
18. Name two ways to create an object in JavaScript.
19. Differentiate between accessing an object property using dot notation vs. bracket notation.
20. What does the `this` keyword refer to when a function is called as a method of an object?

*From Unit III, Topic 6: JavaScript Array, Date, and Math Objects*
21. How do you create an empty array with 5 predefined empty slots in JavaScript?
22. Which array method adds an element to the end of an array?
23. What is the significance of the month parameter in the `new Date(year, month, ...)` constructor?
24. Which `Math` object method is used to generate a random number between 0 (inclusive) and 1 (exclusive)?

*From Unit III, Topic 7: Document Object Model (DOM)*
25. What is the Document Object Model (DOM)?
26. Name two JavaScript methods used to select HTML elements by their ID or class.
27. How do you change the text content of an HTML element using JavaScript?
28. What is the recommended way to add a new HTML element to the end of an existing parent element using JavaScript?

*From Unit III, Topic 8: JavaScript Event Handling*
29. What is an event in JavaScript?
30. What is the recommended method for attaching event handlers in modern JavaScript?
31. What is the purpose of `event.preventDefault()`?
32. Explain the concept of event bubbling.

*From Unit III, Topic 9: Browser Object Model (BOM)*
33. What is the primary function of the Browser Object Model (BOM)?
34. Which object is the top-level object in the BOM hierarchy?
35. Name two properties of the `window` object that provide information about the browser viewport dimensions.
36. How would you programmatically navigate the user to the previous page in their browser history using JavaScript?

*From Unit III, Topic 10: JavaScript Form Handling and Validations*
37. How can you prevent an HTML form from submitting its data normally using JavaScript?
38. What is the purpose of client-side form validation?
39. Why is server-side validation still essential even if client-side validation is implemented?
40. Which HTML5 attribute allows you to specify a regular expression for input validation?

*From Unit III, Topic 11: JavaScript Object-Oriented Techniques*
41. What is the primary purpose of a constructor function in JavaScript?
42. Explain the concept of the prototype chain in JavaScript.
43. How does ES6 `class` syntax relate to JavaScript's prototype-based inheritance?
44. What is the role of the `super()` keyword in class inheritance?

*From Unit III, Topic 12: JSON*
45. What does JSON stand for, and what is its primary purpose?
46. List two valid data types for a JSON value.
47. Which JavaScript method is used to convert a JSON string into a JavaScript object?
48. What is a key syntax rule for property names in JSON?

*From Unit III, Topic 13: Introduction to XML and AJAX*
49. What is the primary difference in purpose between HTML and XML?
50. What does AJAX stand for, and what is its main benefit?
51. Which JavaScript object was traditionally used to make asynchronous HTTP requests in AJAX?
52. Why is JSON often preferred over XML for data exchange in modern AJAX applications?

## Answers

### Section 1: Quiz Questions - Answers
1.  **1. c) `let`** - **Concept:** JavaScript Variables. **Reason:** `let` declares a block-scoped variable, and unlike `const`, its value can be reassigned. `var` is function-scoped.
2.  **2. `"object"`** - **Concept:** `typeof` Operator. **Reason:** This is a well-known historical quirk in JavaScript. `null` is a primitive type, but `typeof null` incorrectly returns `"object"`.
3.  **3. The `Date` object** - **Concept:** Built-in Objects. **Reason:** The `Date` object is the standard built-in object for creating, manipulating, and formatting dates and times.
4.  **4. c) A programming interface for HTML documents** - **Concept:** DOM Definition. **Reason:** The DOM represents the structure of an HTML document as a tree of objects, allowing JavaScript to interact with and modify the page content and structure.
5.  **5. `addEventListener()`** - **Concept:** Event Handling. **Reason:** `addEventListener()` is the modern standard because it allows multiple handlers for a single event, provides more control over the event propagation phase, and is more flexible than older methods.
6.  **6. `window`** - **Concept:** Browser Object Model (BOM). **Reason:** The `window` object is the global object in the browser and serves as the entry point to the entire BOM hierarchy.
7.  **7. `event.preventDefault()`** - **Concept:** Event Object Methods. **Reason:** This method stops the browser from performing the default action associated with an event, which for a form submission is to send the data to the server and reload the page.
8.  **8. `==` performs type coercion, while `===` does not.** - **Concept:** Comparison Operators. **Reason:** `==` (loose equality) will convert operands to the same type before comparing, which can lead to unexpected results (e.g., `5 == "5"` is true). `===` (strict equality) checks for both value and type equality.
9.  **9. `JSON.stringify()`** - **Concept:** JSON in JavaScript. **Reason:** `JSON.stringify()` takes a JavaScript object or value and converts it into a JSON string, which is necessary for sending data to a web server or storing it in `localStorage`.
10. **10. Asynchronous JavaScript and XML** - **Concept:** AJAX Definition. **Reason:** AJAX is a set of techniques for making asynchronous requests from the browser to the server to update a page without a full reload.

### Section 2: Reasoning Questions - Answers
1.  **1. Explanation:**
    -   **`var`**: Function-scoped, can be re-declared and re-assigned, and is hoisted with an initial value of `undefined`.
    -   **`let`**: Block-scoped, can be re-assigned but not re-declared in the same scope. It is hoisted but not initialized (temporal dead zone).
    -   **`const`**: Block-scoped, cannot be re-assigned or re-declared. It must be initialized at declaration.
    **Concept:** Variable Scopes. **Reason:** `var` is avoided because its function-scoping and hoisting behavior can lead to bugs and unexpected results, especially in loops and conditional blocks. `let` and `const` provide more predictable, block-level scoping.
2.  **2. Explanation:** A closure is an inner function that has access to the variables of its outer (enclosing) function, even after the outer function has finished executing.
    ```javascript
    function makeCounter() {
        let count = 0;
        return function() {
            count++;
            return count;
        };
    }
    const counter = makeCounter();
    console.log(counter()); // 1
    console.log(counter()); // 2
    ```
    **Concept:** Closures. **Reason:** The inner function "closes over" the `count` variable from its lexical environment. Each time `makeCounter` is called, a new, private `count` is created, which the returned inner function "remembers" and can modify.
3.  **3. Explanation:** The **DOM (Document Object Model)** represents the HTML document itself (the content of the page). It allows JavaScript to manipulate elements, styles, and content. The **BOM (Browser Object Model)** represents the browser window and its surrounding environment. **Concept:** DOM vs. BOM. **Reason:** An example from the DOM is the `document` object (`document.getElementById`). An example from the BOM is the `window` object (`window.location` or `window.history`).
4.  **4. Explanation:** Event bubbling is the phase of event propagation where an event, after firing on the target element, travels (or "bubbles") up through its parent elements in the DOM tree, firing listeners on each parent along the way. **Concept:** Event Propagation. **Reason:** You can stop it by calling the `event.stopPropagation()` method within an event handler. This prevents the event from traveling to any subsequent parent elements.
5.  **5. Explanation:** Every JavaScript object has a hidden link to another object, called its **prototype**. That prototype object has its own prototype, and so on, until an object is reached with `null` as its prototype. This sequence is the prototype chain. **Concept:** Prototypal Inheritance. **Reason:** When you try to access a property on an object, JavaScript will look for it on the object itself, then on its prototype, then on the prototype's prototype, and so on up the chain. This is how JavaScript implements inheritance.
6.  **6. Explanation:** `localStorage` can only store string values. **Concept:** Web Storage & Data Types. **Reason:** To store a complex data type like a JavaScript object, you must first convert it into its string representation. `JSON.stringify()` is the standard way to do this. To read it back, you must then use `JSON.parse()` to convert the string back into a usable JavaScript object.
7.  **7. Explanation:**
    -   **Syntax:** JSON is stricter; keys must be double-quoted strings. XML uses opening and closing tags.
    -   **Verbosity:** JSON is much less verbose and results in smaller file sizes.
    -   **Parsing:** JSON is parsed natively in JavaScript (`JSON.parse()`), while XML requires a more complex XML parser.
    **Concept:** Data Interchange Formats. **Reason:** These differences make JSON generally faster and easier to work with in the context of web APIs and JavaScript applications.
8.  **8. Explanation:** The `this` keyword is a reference to the object that is currently executing the function. Its value is determined by the "call site" (how the function is called). **Concept:** The `this` Keyword. **Reason:** When called as a method of an object (e.g., `myObj.myMethod()`), `this` refers to `myObj`. When called as a standalone function (e.g., `myMethod()`), `this` in non-strict mode refers to the global `window` object, while in strict mode it is `undefined`.
9.  **9. Explanation:**
    -   **`innerHTML`**: Gets or sets the full HTML content inside an element, including any HTML tags.
    -   **`textContent`**: Gets or sets only the raw text content, ignoring and stripping out any HTML tags.
    **Concept:** DOM Manipulation. **Reason:** You should prefer `textContent` when you only want to work with plain text, as it is faster and more secure (it prevents HTML injection attacks). Use `innerHTML` only when you explicitly need to parse and render HTML tags.
10. **10. Explanation:** An AJAX request is asynchronous, meaning that when JavaScript sends the request, it does not wait for the response. It continues executing other code immediately. **Concept:** AJAX Asynchronicity. **Reason:** The `onload` or `onreadystatechange` event handler is a callback function that JavaScript registers. This function is automatically executed only when the server's response is fully received, allowing the application to process the data without freezing the user interface while waiting.

### Section 3: Real-World Cases - Answers
1.  **1. Case: A "Dark Mode" Toggle**
    *   **Object:** `localStorage`.
    *   **Concept:** `localStorage` vs. `sessionStorage`. **Reason:** `localStorage` should be used because its data persists indefinitely, even after the browser is closed. This ensures that when the user returns to the site, their "dark mode" preference can be retrieved and applied, providing a consistent experience across sessions.
2.  **2. Case: Interactive To-Do List**
    *   **Event:** The `click` event.
    *   **Implementation:** You would attach an event listener to the parent `<ul>` or `<div>` containing the list (using event delegation). Inside the handler, you would check if `event.target` is a list item (`<li>`). If it is, you would use `event.target.classList.toggle('completed')` to add or remove the `completed` class, which would then apply the line-through style.
    **Concept:** Event Handling & Delegation. **Reason:** Event delegation is efficient because it only requires one listener on the parent element, and it will work even for new to-do items added dynamically.
3.  **3. Case: Form Validation**
    *   **Event:** The `submit` event on the `<form>` element.
    *   **Action:** Inside the event handler, you would first call `event.preventDefault()` to stop the form from submitting. Then, you would compare the `.value` of the password field with the `.value` of the confirm password field. If they don't match, you would display an error message to the user and do nothing further. If they do match, you would then allow the form to submit or send the data via AJAX.
    **Concept:** Form Handling & Validation. **Reason:** Using the `submit` event is the most reliable way to catch the final submission attempt and perform all necessary validation checks at once.
4.  **4. Case: A Countdown Timer**
    *   **Method:** `window.setInterval(function, delay)`.
    *   **Concept:** BOM Timers. **Reason:** `setInterval()` is designed to execute a function repeatedly at a specified interval. You would use `setInterval(updateTimer, 1000)` to call an `updateTimer` function every 1000 milliseconds (1 second), which would then update the timer display on the page.
5.  **5. Case: Dynamic Content Loading**
    *   **Technology:** **AJAX**.
    *   **Data Format:** **JSON** would be ideal.
    **Concept:** AJAX & JSON. **Reason:** When the "Load More" button is clicked, JavaScript would use AJAX (via `fetch` or `XMLHttpRequest`) to make an asynchronous `GET` request to the server. The server would respond with the next 10 posts formatted as a JSON array. JSON is ideal because it's lightweight and easily parsed by JavaScript into an array of objects, which can then be looped through to dynamically create and append new HTML elements to the page.
6.  **6. Case: Creating Multiple User Objects**
    *   **Approach:** A **`class`** (or constructor function) would be far more appropriate.
    *   **Concept:** OOP in JavaScript. **Reason:** Using a class provides a reusable blueprint for creating `User` objects. This ensures that every user object is created with a consistent structure (`name`, `email`) and has access to the same shared methods (like `login()`) through the prototype, which is much more efficient and maintainable than duplicating the logic for every single user object literal.
7.  **7. Case: Accessing Nested Data**
    *   **Code:**
        ```javascript
        const jsonString = '{"id": 1, "data": {"status": "active"}}';
        const dataObject = JSON.parse(jsonString);
        const status = dataObject.data.status;
        console.log(status); // "active"
        ```
    *   **Concept:** `JSON.parse()` and Object Access. **Reason:** You must first parse the JSON string into a JavaScript object. Then, you can use dot notation to traverse the nested object structure to access the desired property.
8.  **8. Case: A Simple Calculator**
    *   **Object:** The built-in `Math` object.
    *   **Concept:** Built-in Objects. **Reason:** The `Math` object provides static methods for a wide range of mathematical operations, such as `Math.sqrt()` for square root and `Math.round()` for rounding, which are essential for a calculator.
9.  **9. Case: Navigating Browser History**
    *   **Method:** You would use the `history.back()` method from the BOM.
    *   **Implementation:**
        ```javascript
        document.getElementById('myBackButton').addEventListener('click', function() {
            history.back();
        });
        ```
    **Concept:** Browser Object Model (BOM). **Reason:** The `history` object provides a direct programmatic interface to control the browser's session history, allowing you to mimic the native back and forward buttons.
10. **10. Case: A "Hoisting" Pitfall**
    *   **Output:** `undefined`.
    *   **Concept:** Hoisting. **Reason:** In JavaScript, declarations made with `var` are "hoisted" to the top of their scope during the compilation phase, but their assignments are not. So, the code is interpreted as if it were:
        ```javascript
        var myVar; // Declaration is hoisted, myVar is initialized with undefined
        console.log(myVar); // Logs undefined
        myVar = 10; // Assignment happens here
        ```

### Section 4: Rapid Fire Questions - Answers
1.  **1. What keyword is used to declare a constant variable?** `const`.
2.  **2. Which operator checks for both value and type equality?** `===` (strict equality).
3.  **3. What is the output of `10 + "5"`?** `"105"` (a string).
4.  **4. Which array method adds an element to the end of an array?** `push()`.
5.  **5. What is the index of the first element in an array?** `0`.
6.  **6. Which method is used to select the first element that matches a CSS selector?** `document.querySelector()`.
7.  **7. What event is fired when a user clicks an element?** The `click` event.
8.  **8. Which object in the BOM contains information about the current URL?** The `location` object.
9.  **9. What does `JSON.parse()` do?** It converts a JSON string into a JavaScript object.
10. **10. What is the modern, promise-based alternative to `XMLHttpRequest`?** The `fetch` API.

### Section 5: All Possible 2-Mark Remember Questions - Answers
1.  **1. What is the primary role of JavaScript in web development?** - **Concept:** JavaScript Role. **Reason:** JavaScript is primarily used for client-side scripting to create dynamic and interactive web pages, responding to user actions and manipulating page content.
2.  **2. Differentiate between JavaScript and ECMAScript.** - **Concept:** JS vs. ECMA. **Reason:** ECMAScript is the standardized specification for a scripting language, while JavaScript is the most popular implementation of that standard.
3.  **3. List two core features of JavaScript.** - **Concept:** JS Features. **Reason:** Dynamically typed, event-driven, prototype-based OOP, first-class functions (any two).
4.  **4. What is the recommended way to include JavaScript in an HTML document for larger projects, and why?** - **Concept:** External Scripts. **Reason:** External `.js` files (`<script src="...">`) are recommended for organization, reusability, and browser caching.
5.  **5. Differentiate between `var` and `let` in JavaScript.** - **Concept:** Variable Scopes. **Reason:** `var` is function-scoped and hoisted, while `let` is block-scoped and not initialized before declaration (temporal dead zone).
6.  **6. What is the purpose of the `const` keyword, and what is a key limitation when used with objects?** - **Concept:** Constants. **Reason:** `const` declares a read-only constant. For objects, it prevents re-assignment of the variable, but does not make the object's properties immutable.
7.  **7. List three primitive data types in JavaScript.** - **Concept:** Data Types. **Reason:** `string`, `number`, `boolean`, `null`, `undefined` (any three).
8.  **8. What is type coercion in JavaScript, and why can it be problematic?** - **Concept:** Type Coercion. **Reason:** It's the automatic conversion of values between types, which can be problematic as it may lead to unexpected results (e.g., `10 + "5" === "105"`).
9.  **9. Differentiate between `==` and `===` operators in JavaScript.** - **Concept:** Equality Operators. **Reason:** `==` (loose equality) performs type coercion before comparing, while `===` (strict equality) compares both value and type.
10. **10. What is the purpose of the `&&` operator?** - **Concept:** Logical Operators. **Reason:** The `&&` (logical AND) operator returns `true` only if both of its operands are `true`.
11. **11. Give an example of an expression in JavaScript.** - **Concept:** Expressions. **Reason:** `10 + 5` or `x > 10` are examples of code that resolves to a single value.
12. **12. Name two control flow statements in JavaScript.** - **Concept:** Control Flow. **Reason:** `if...else`, `for` loop, `while` loop, `switch`.
13. **13. Differentiate between a function declaration and a function expression.** - **Concept:** Functions. **Reason:** Function declarations are hoisted (can be called before definition), while function expressions are not.
14. **14. What is the primary difference between global scope and function scope?** - **Concept:** Scope. **Reason:** Global scope variables are accessible everywhere, while function-scoped variables are only accessible within their defining function.
15. **15. Explain the concept of a closure in JavaScript.** - **Concept:** Closures. **Reason:** A closure is an inner function that has access to its outer function's variables, even after the outer function has executed.
16. **16. What is hoisting in JavaScript?** - **Concept:** Hoisting. **Reason:** Hoisting is a mechanism where variable and function declarations are moved to the top of their scope before code execution.
17. **17. What is a JavaScript object?** - **Concept:** Objects. **Reason:** An object is a complex data type that stores a collection of key-value pairs.
18. **18. Name two ways to create an object in JavaScript.** - **Concept:** Object Creation. **Reason:** Object literal syntax (`{}`) and constructor functions (`new Object()`).
19. **19. Differentiate between accessing an object property using dot notation vs. bracket notation.** - **Concept:** Property Access. **Reason:** Dot notation (`obj.key`) is used for static keys, while bracket notation (`obj['key']`) is used for dynamic or variable keys.
20. **20. What does the `this` keyword refer to when a function is called as a method of an object?** - **Concept:** `this` Keyword. **Reason:** It refers to the object that the method was called on.
21. **21. How do you create an empty array with 5 predefined empty slots in JavaScript?** - **Concept:** Arrays. **Reason:** `const arr = new Array(5);`.
22. **22. Which array method adds an element to the end of an array?** - **Concept:** Array Methods. **Reason:** The `push()` method.
23. **23. What is the significance of the month parameter in the `new Date(year, month, ...)` constructor?** - **Concept:** Date Object. **Reason:** The month is zero-indexed (0 for January, 11 for December).
24. **24. Which `Math` object method is used to generate a random number between 0 (inclusive) and 1 (exclusive)?** - **Concept:** Math Object. **Reason:** `Math.random()`.
25. **25. What is the Document Object Model (DOM)?** - **Concept:** DOM Definition. **Reason:** The DOM is a programming interface for HTML documents that represents the page as a tree of objects for manipulation.
26. **26. Name two JavaScript methods used to select HTML elements by their ID or class.** - **Concept:** DOM Selection. **Reason:** `document.getElementById()` and `document.getElementsByClassName()`.
27. **27. How do you change the text content of an HTML element using JavaScript?** - **Concept:** DOM Manipulation. **Reason:** Using the `element.textContent` or `element.innerHTML` properties.
28. **28. What is the recommended way to add a new HTML element to the end of an existing parent element using JavaScript?** - **Concept:** DOM Manipulation. **Reason:** Using `parentNode.appendChild(childNode)`.
29. **29. What is an event in JavaScript?** - **Concept:** Events. **Reason:** An event is an action that occurs in the browser, such as a user click or page load, that JavaScript can respond to.
30. **30. What is the recommended method for attaching event handlers in modern JavaScript?** - **Concept:** Event Handling. **Reason:** The `addEventListener()` method.
31. **31. What is the purpose of `event.preventDefault()`?** - **Concept:** Event Object. **Reason:** It stops the browser's default action for an event, such as a form submitting.
32. **32. Explain the concept of event bubbling.** - **Concept:** Event Propagation. **Reason:** Event bubbling is when an event travels up from the target element through its parent elements in the DOM tree.
33. **33. What is the primary function of the Browser Object Model (BOM)?** - **Concept:** BOM Definition. **Reason:** The BOM allows JavaScript to interact with the browser window and its environment, outside of the document content.
34. **34. Which object is the top-level object in the BOM hierarchy?** - **Concept:** BOM. **Reason:** The `window` object.
35. **35. Name two properties of the `window` object that provide information about the browser viewport dimensions.** - **Concept:** Window Object. **Reason:** `window.innerWidth` and `window.innerHeight`.
36. **36. How would you programmatically navigate the user to the previous page in their browser history using JavaScript?** - **Concept:** History Object. **Reason:** By calling the `history.back()` method.
37. **37. How can you prevent an HTML form from submitting its data normally using JavaScript?** - **Concept:** Form Handling. **Reason:** By calling `event.preventDefault()` in the form's `submit` event listener.
38. **38. What is the purpose of client-side form validation?** - **Concept:** Form Validation. **Reason:** To provide immediate feedback to the user and reduce unnecessary server requests.
39. **39. Why is server-side validation still essential even if client-side validation is implemented?** - **Concept:** Validation Security. **Reason:** Client-side validation can be bypassed, so server-side validation is mandatory for security and data integrity.
40. **40. Which HTML5 attribute allows you to specify a regular expression for input validation?** - **Concept:** Form Validation. **Reason:** The `pattern` attribute.
41. **41. What is the primary purpose of a constructor function in JavaScript?** - **Concept:** OOP. **Reason:** To serve as a blueprint for creating multiple objects of the same type.
42. **42. Explain the concept of the prototype chain in JavaScript.** - **Concept:** Prototypal Inheritance. **Reason:** It's the mechanism by which objects inherit properties and methods from other objects.
43. **43. How does ES6 `class` syntax relate to JavaScript's prototype-based inheritance?** - **Concept:** ES6 Classes. **Reason:** It is syntactic sugar over the existing prototype-based inheritance, providing a cleaner syntax.
44. **44. What is the role of the `super()` keyword in class inheritance?** - **Concept:** Class Inheritance. **Reason:** It calls the constructor of the parent class.
45. **45. What does JSON stand for, and what is its primary purpose?** - **Concept:** JSON Definition. **Reason:** JavaScript Object Notation; its purpose is to be a lightweight data-interchange format.
46. **46. List two valid data types for a JSON value.** - **Concept:** JSON Data Types. **Reason:** `string`, `number`, `boolean`, `null`, `object`, `array`.
47. **47. Which JavaScript method is used to convert a JSON string into a JavaScript object?** - **Concept:** JSON Parsing. **Reason:** `JSON.parse()`.
48. **48. What is a key syntax rule for property names in JSON?** - **Concept:** JSON Syntax. **Reason:** Property names must be enclosed in double quotes.
49. **49. What is the primary difference in purpose between HTML and XML?** - **Concept:** XML vs. HTML. **Reason:** HTML is for displaying data, while XML is for describing and carrying data.
50. **50. What does AJAX stand for, and what is its main benefit?** - **Concept:** AJAX. **Reason:** Asynchronous JavaScript and XML; its main benefit is updating parts of a web page without a full reload.
51. **51. Which JavaScript object was traditionally used to make asynchronous HTTP requests in AJAX?** - **Concept:** AJAX. **Reason:** The `XMLHttpRequest` (XHR) object.
52. **52. Why is JSON often preferred over XML for data exchange in modern AJAX applications?** - **Concept:** JSON vs. XML. **Reason:** JSON is lighter, less verbose, and easier for JavaScript to parse natively.
