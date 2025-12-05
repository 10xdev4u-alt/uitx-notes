---
title: "FAT02 - 2024 - Answer Key"
id: fat02-2k24-anx
tags:
  - fat
  - answers
  - unit-2
  - unit-3
aliases:
  - "FAT02 Answers"
links:
  - "[[UITx/fat02_2k24.md|FAT02 Question Paper]]"
---

# CS22503 - User Interface Tools and Techniques
## FAT02 - Answer Key

> [!note] This document provides detailed answers for the FAT02 (2024-2025) question paper, focusing on CSS3 styling and core JavaScript concepts.

---

## PART A (10 x 2 = 20 Marks)

**1. List out any four border style effects with an example code.**

Four common border style effects are `solid`, `dotted`, `dashed`, and `double`. These are values for the `border-style` CSS property.

**Example Code:**
```css
/* A solid red border */
.solid-border {
    border: 2px solid red;
}

/* A dotted blue border */
.dotted-border {
    border: 2px dotted blue;
}

/* A dashed green border */
.dashed-border {
    border: 2px dashed green;
}

/* A double black border */
.double-border {
    border: 4px double black;
}
```

---

**2. Create an animation with 3 seconds delay from backward to forward.**

This requires using `animation-delay` and setting `animation-direction` to `alternate`.

**Example Code:**
```css
@keyframes slide-in {
  from {
    transform: translateX(-100px);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

.animated-element {
  animation-name: slide-in;
  animation-duration: 2s;
  animation-delay: 3s; /* 3-second delay before starting */
  animation-direction: alternate; /* Plays forward, then backward */
  animation-iteration-count: infinite; /* Loop indefinitely */
}
```

---

**3. Differentiate the declaration of a variable using `var` and `let`.**

| Feature | `var` | `let` |
| :--- | :--- | :--- |
| **Scope** | **Function-scoped**. A `var` variable is accessible throughout the function it is declared in. | **Block-scoped**. A `let` variable is only accessible within the block (`{...}`) it is declared in. |
| **Hoisting** | Declarations are hoisted to the top of their scope and initialized with `undefined`. | Declarations are hoisted but not initialized, creating a "temporal dead zone" until the declaration is encountered. |
| **Re-declaration** | Can be re-declared in the same scope without error. | Cannot be re-declared in the same scope. |

---

**4. Write a JavaScript program to greet the user with a welcome message.**

This can be done using a simple function and the `alert()` method to display a popup message.

```javascript
function greetUser(name) {
  // Create the welcome message
  const message = `Welcome, ${name}! We are glad to have you here.`;
  
  // Display the message in an alert box
  alert(message);
}

// Call the function to greet the user
greetUser("Macha");
```

---

**5. List out the built in objects in Javascript.**

JavaScript includes several standard built-in objects that are fundamental for common operations. Key examples include:
-   **`Object`**: The base object for all other objects.
-   **`Array`**: For managing ordered collections of data.
-   **`Date`**: For working with dates and times.
-   **`Math`**: For mathematical constants and functions.
-   **`String`**: For string manipulation.
-   **`Number`**: For numeric operations.
-   **`Boolean`**: For true/false values.
-   **`JSON`**: For parsing and stringifying JSON data.

---

**6. How do you create an array in Javascript? Give an example.**

There are two primary ways to create an array in JavaScript:

1.  **Array Literal (Recommended):** This is the simplest and most common method.
    ```javascript
    const fruits = ["Apple", "Banana", "Cherry"];
    ```

2.  **`new Array()` Constructor:**
    ```javascript
    const cars = new Array("Ford", "BMW", "Audi");
    ```

**Example:**
```javascript
// Using array literal
let colors = ["Red", "Green", "Blue"];
console.log(colors[0]); // Accessing the first element: "Red"
```

---

**7. What are the various control statements in Javascript?**

Control statements are used to control the flow of execution in a program. The main types are:
1.  **Conditional Statements:**
    -   `if...else`
    -   `if...else if...else`
    -   `switch`
2.  **Looping (Iterative) Statements:**
    -   `for`
    -   `while`
    -   `do...while`
    -   `for...in` (for iterating over object properties)
    -   `for...of` (for iterating over iterable objects like arrays)

---

**8. List out the various Form controls and how do you validate them?**

**Form Controls:**
-   `<input>` (with types like `text`, `password`, `checkbox`, `radio`, `submit`, `date`, `email`, etc.)
-   `<textarea>`: For multi-line text input.
-   `<select>`: For creating a drop-down list.
-   `<button>`: For clickable buttons.

**Validation Methods:**
1.  **HTML5 Built-in Validation:** Using attributes like `required` (must be filled), `type="email"` (must be a valid email format), `pattern` (must match a regex), `minlength`, and `maxlength`.
2.  **JavaScript Custom Validation:** By attaching an event listener to the form's `submit` event, preventing the default submission with `event.preventDefault()`, and then checking the input values against custom logic (e.g., checking if two password fields match).

---

**9. What is the purpose of JSON?**

**JSON (JavaScript Object Notation)** is a lightweight, text-based data-interchange format. Its primary purpose is to transmit data between a server and a web application (or between two servers) in a format that is easy for both humans to read and machines to parse. It has become the de facto standard for web APIs.

---

**10. What is the concept behind AJAX in webpage?**

**AJAX (Asynchronous JavaScript and XML)** is a set of web development techniques that allows a web page to communicate with a server **asynchronously** in the background. The core concept is to update parts of a web page with new data from the server **without requiring a full page reload**, leading to a faster, more dynamic, and more responsive user experience.

---

## PART B (3 x 10 = 30 Marks)

**11. (a) Write a HTML and CSS program to demonstrate transition and animation effects with `<div>` element.**

This program demonstrates a `transition` on hover and a continuous `animation`.

**HTML (`index.html`):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Transition and Animation Demo</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>CSS Transition and Animation</h1>
    <div class="box">Hover over me!</div>
</body>
</html>
```

**CSS (`style.css`):**
```css
/* Define the keyframes for the animation */
@keyframes pulse {
  0% {
    transform: scale(1);
    box-shadow: 0 0 5px rgba(0,0,0,0.2);
  }
  50% {
    transform: scale(1.05);
    box-shadow: 0 0 20px rgba(0,123,255,0.5);
  }
  100% {
    transform: scale(1);
    box-shadow: 0 0 5px rgba(0,0,0,0.2);
  }
}

.box {
  width: 200px;
  height: 200px;
  background-color: #007bff;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  margin: 50px auto;
  
  /* 1. Define the transition effect for hover */
  transition: transform 0.4s ease-in-out, 
              background-color 0.4s ease,
              border-radius 0.4s ease;

  /* 2. Apply the keyframe animation */
  animation-name: pulse;
  animation-duration: 3s;
  animation-iteration-count: infinite;
}

/* State change that triggers the transition */
.box:hover {
  background-color: #ff4500;
  transform: rotate(360deg);
  border-radius: 50%; /* Becomes a circle on hover */
}
```

**Explanation:**
1.  **Transition:** The `.box` class has a `transition` property. When the user hovers over the box, the `transform` (rotation), `background-color`, and `border-radius` properties change smoothly over 0.4 seconds.
2.  **Animation:** The `@keyframes pulse` rule defines an animation that scales the box up and adds a glowing shadow, then returns to normal. The `animation` property applies this `pulse` animation to the `.box`, making it run for 3 seconds and loop infinitely.

---

**11. (b) Create and style a webpage with the following CSS properties: i) 2D transformations ii) Multiple background images iii) Image border**

**HTML (`index.html`):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Advanced CSS Styling</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Advanced CSS Properties Demo</h1>
    
    <div class="transformed-box">2D Transform</div>
    
    <div class="multi-bg-box">Multiple Backgrounds</div>
    
    <div class="image-border-box">Image Border</div>
</body>
</html>
```

**CSS (`style.css`):**
```css
body {
    font-family: sans-serif;
    padding: 20px;
}

/* i) 2D Transformations */
.transformed-box {
    width: 200px;
    height: 100px;
    background-color: #28a745;
    color: white;
    text-align: center;
    line-height: 100px;
    margin: 50px;
    transition: transform 0.5s ease;
}
.transformed-box:hover {
    transform: rotate(10deg) scale(1.2) translateX(20px) skewY(-5deg);
}

/* ii) Multiple Background Images */
.multi-bg-box {
    width: 100%;
    height: 300px;
    color: white;
    font-size: 3em;
    text-align: center;
    line-height: 300px;
    margin: 50px 0;
    background-image: url('overlay.png'), url('background.jpg');
    background-repeat: no-repeat, repeat;
    background-position: center, top left;
    background-size: 50%, auto;
}

/* iii) Image Border */
.image-border-box {
    width: 250px;
    height: 150px;
    padding: 20px;
    margin: 50px;
    text-align: center;
    
    /* Define a border to be replaced by the image */
    border: 30px solid transparent;
    
    /* Apply the border image */
    border-image-source: url('border-pattern.png');
    border-image-slice: 30;
    border-image-repeat: round;
}
```
*(Note: For this to work, you would need to have the image files `overlay.png`, `background.jpg`, and `border-pattern.png` in the same directory.)*

---

**12. (a) Write a JavaScript program to find the: i) Summation of n ii) Summation of square of n numbers.**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>JS Summation</title>
</head>
<body>
    <h2>Summation Calculator</h2>
    <label for="numberInput">Enter a number (n):</label>
    <input type="number" id="numberInput" value="5">
    <button onclick="calculate()">Calculate</button>
    <div id="results"></div>

    <script>
        function calculate() {
            const n = parseInt(document.getElementById('numberInput').value);
            const resultsDiv = document.getElementById('results');

            if (isNaN(n) || n < 0) {
                resultsDiv.innerHTML = "<p>Please enter a valid positive number.</p>";
                return;
            }

            // i) Summation of n
            let sum = 0;
            for (let i = 1; i <= n; i++) {
                sum += i;
            }

            // ii) Summation of square of n numbers
            let sumOfSquares = 0;
            for (let i = 1; i <= n; i++) {
                sumOfSquares += i * i;
            }

            resultsDiv.innerHTML = `
                <p>For n = ${n}:</p>
                <p>Summation (1 to n): ${sum}</p>
                <p>Summation of Squares (1² to n²): ${sumOfSquares}</p>
            `;
        }
    </script>
</body>
</html>
```

---

**12. (b) Explain in detail about AJAX architecture with an example code snippet.**

**AJAX (Asynchronous JavaScript and XML)** is a set of techniques for creating fast and dynamic web pages. It allows a web page to update content asynchronously by exchanging small amounts of data with the server behind the scenes, without requiring a full page reload.

**AJAX Architecture (The Flow):**

1.  **Event Trigger:** An event occurs in the browser (e.g., a user clicks a button).
2.  **XHR Object Creation:** JavaScript creates an `XMLHttpRequest` object (or uses the modern `fetch` API).
3.  **Request Configuration:** The XHR object is configured with the server URL, HTTP method (`GET` or `POST`), and a callback function to handle the response.
4.  **Asynchronous Request:** The request is sent to the server. Because it's asynchronous, the user can continue to interact with the page; the browser does not freeze.
5.  **Server Processing:** The server receives the request, processes it (e.g., queries a database), and prepares a response, typically in JSON or XML format.
6.  **Response Handling:** When the response is ready, the server sends it back. The XHR object's callback function is triggered.
7.  **DOM Update:** The JavaScript callback function processes the response data and updates the relevant part of the HTML page using the DOM.

**Example Code Snippet (using `XMLHttpRequest`):**

This example fetches user data from a public API when a button is clicked.

```html
<!DOCTYPE html>
<html>
<head>
    <title>AJAX Demo</title>
</head>
<body>
    <h2>AJAX User Fetcher</h2>
    <button id="loadUserBtn">Load User Data</button>
    <div id="userInfo"></div>

    <script>
        document.getElementById('loadUserBtn').addEventListener('click', function() {
            // 1. Create an XMLHttpRequest object
            const xhr = new XMLHttpRequest();
            
            // 2. Configure the request
            xhr.open('GET', 'https://jsonplaceholder.typicode.com/users/1', true); // true for asynchronous

            // 3. Set up the callback function for when the request completes
            xhr.onload = function() {
                if (this.status === 200) {
                    // Success!
                    const user = JSON.parse(this.responseText);
                    const output = `
                        <ul>
                            <li><strong>Name:</strong> ${user.name}</li>
                            <li><strong>Email:</strong> ${user.email}</li>
                            <li><strong>Website:</strong> ${user.website}</li>
                        </ul>
                    `;
                    // 4. Update the DOM
                    document.getElementById('userInfo').innerHTML = output;
                } else {
                    // Error
                    document.getElementById('userInfo').innerHTML = `Error: ${this.status}`;
                }
            };
            
            // Handle network errors
            xhr.onerror = function() {
                console.log('Request Error...');
            };

            // 5. Send the request
            xhr.send();
            document.getElementById('userInfo').innerHTML = 'Loading...';
        });
    </script>
</body>
</html>
```

---

**13. (a) Write a Javascript program to demonstrate various mouse events with output.**

This program will track and display different mouse events as they occur on a specific `div`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Mouse Events Demo</title>
    <style>
        #eventBox {
            width: 300px;
            height: 200px;
            border: 2px solid black;
            background-color: lightblue;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        #output {
            border: 1px solid #ccc;
            padding: 10px;
            height: 150px;
            overflow-y: scroll;
        }
    </style>
</head>
<body>
    <h2>Mouse Event Tracker</h2>
    <div id="eventBox">Hover, Click, or Move Mouse Here</div>
    <div id="output">Event log will appear here...</div>

    <script>
        const eventBox = document.getElementById('eventBox');
        const output = document.getElementById('output');

        function logEvent(eventName, event) {
            let logMessage = `${eventName} fired.`;
            if (eventName === 'mousemove') {
                logMessage += ` Coords: (X: ${event.clientX}, Y: ${event.clientY})`;
            }
            output.innerHTML = logMessage + '<br>' + output.innerHTML;
        }

        // Attach event listeners
        eventBox.addEventListener('click', (e) => logEvent('click', e));
        eventBox.addEventListener('dblclick', (e) => logEvent('dblclick', e));
        eventBox.addEventListener('mousedown', (e) => logEvent('mousedown', e));
        eventBox.addEventListener('mouseup', (e) => logEvent('mouseup', e));
        eventBox.addEventListener('mouseover', (e) => logEvent('mouseover', e));
        eventBox.addEventListener('mouseout', (e) => logEvent('mouseout', e));
        eventBox.addEventListener('mousemove', (e) => logEvent('mousemove', e));
    </script>
</body>
</html>
```
**Output Explanation:**
-   When you move your mouse into the blue box, `mouseover` will fire.
-   As you move your mouse around inside the box, `mousemove` will fire continuously, showing the coordinates.
-   When you press the mouse button down, `mousedown` fires.
-   When you release it, `mouseup` fires, immediately followed by `click`.
-   If you click twice quickly, `dblclick` will fire.
-   When your mouse leaves the box, `mouseout` fires.

---

**13. (b) Write a JavaScript program to find out factorial using both recursive and non-recursive version.**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Factorial Calculator</title>
</head>
<body>
    <h2>Factorial Calculator</h2>
    <label for="factInput">Enter a number:</label>
    <input type="number" id="factInput" value="5">
    <button onclick="calculateFactorial()">Calculate</button>
    <div id="factorialResult"></div>

    <script>
        // 1. Non-Recursive (Iterative) Version
        function factorial_nonRecursive(n) {
            if (n < 0) return "Not defined for negative numbers";
            if (n === 0 || n === 1) return 1;
            
            let result = 1;
            for (let i = 2; i <= n; i++) {
                result *= i;
            }
            return result;
        }

        // 2. Recursive Version
        function factorial_recursive(n) {
            if (n < 0) return "Not defined for negative numbers";
            
            // Base case
            if (n === 0 || n === 1) {
                return 1;
            }
            // Recursive step
            else {
                return n * factorial_recursive(n - 1);
            }
        }

        function calculateFactorial() {
            const num = parseInt(document.getElementById('factInput').value);
            const resultDiv = document.getElementById('factorialResult');

            if (isNaN(num)) {
                resultDiv.innerHTML = "<p>Please enter a valid number.</p>";
                return;
            }

            const nonRecursiveResult = factorial_nonRecursive(num);
            const recursiveResult = factorial_recursive(num);

            resultDiv.innerHTML = `
                <p>For n = ${num}:</p>
                <p>Factorial (Non-Recursive): ${nonRecursiveResult}</p>
                <p>Factorial (Recursive): ${recursiveResult}</p>
            `;
        }
    </script>
</body>
</html>
```
**Explanation:**
-   **Non-Recursive:** This version uses a `for` loop to multiply numbers from 2 up to `n`, accumulating the result in a variable. It's generally more memory-efficient for large numbers.
-   **Recursive:** This version defines a "base case" (when `n` is 0 or 1) to stop the recursion. For any other number, it calls itself with `n-1` and multiplies the result by `n`. It's often more elegant but can lead to stack overflow errors for very large numbers.