---
title: "FAT02 - 2025 - Answer Key"
id: fat02-2k25-anx
tags:
  - fat
  - answers
  - unit-2
  - unit-3
aliases:
  - "FAT02 2025 Answers"
links:
  - "[[UITx/fat02_2k25.md|FAT02 2025 Question Paper]]"
---

# CS22503 - User Interface Tools and Techniques
## FAT02 - 2025 - Answer Key

> [!note] This document provides detailed answers for the FAT02 (2025) question paper, focusing on CSS3 and JavaScript.

---

## PART A (10 x 2 = 20 Marks)

**1. Compare inline CSS and external CSS in terms of maintainability with an example.**

| Feature | Inline CSS | External CSS |
| :--- | :--- | :--- |
| **Maintainability** | **Low**. Styles are mixed directly with HTML content, making it very difficult to update styles across multiple elements or pages. | **High**. Styles are defined in a separate `.css` file, allowing you to change the look of an entire site by editing just one file. |
| **Example** | `<p style="color: blue; font-size: 16px;">Text</p>` | **HTML:** `<link rel="stylesheet" href="styles.css"> <p class="info-text">Text</p>` <br> **CSS:** `.info-text { color: blue; font-size: 16px; }` |

Using external CSS is far more maintainable because if you need to change the color of all `info-text` paragraphs, you only need to edit one line in `styles.css`. With inline CSS, you would have to find and change every single `<p>` tag.

---

**2. Write the CSS code to give a heading (`<h1>`) a black shadow with 5px horizontal and 3px vertical offset.**

You can achieve this using the `text-shadow` property.

```css
h1 {
  text-shadow: 5px 3px black;
}
```
-   `5px`: The horizontal offset (to the right).
-   `3px`: The vertical offset (downwards).
-   `black`: The color of the shadow.

---

**3. Sketch the CSS box model.**

The CSS box model describes the rectangular boxes that are generated for elements in the document tree. Each box has four edges: content, padding, border, and margin.

**Sketch:**
```
+---------------------------------------------------+
|                      Margin                       |
|   +-------------------------------------------+   |
|   |                   Border                    |   |
|   |   +-----------------------------------+   |   |
|   |   |              Padding              |   |   |
|   |   |   +---------------------------+   |   |   |
|   |   |   |                           |   |   |   |
|   |   |   |          Content          |   |   |   |
|   |   |   |                           |   |   |   |
|   |   |   +---------------------------+   |   |   |
|   |   |                                   |   |   |
|   |   +-----------------------------------+   |   |
|   |                                           |   |
|   +-------------------------------------------+   |
|                                                 |
+---------------------------------------------------+
```

---

**4. Apply two box-shadows on a `<div>`: the first shadow should be 10px right, 5px down, 15px blur, gray color, and the second shadow should be 5px left, 8px up, 10px blur, semi-transparent black color appearing inside the `<div>`.**

You can apply multiple shadows by separating them with a comma. The `inset` keyword is used for the inner shadow.

```css
div {
  box-shadow: 10px 5px 15px gray, 
              inset -5px -8px 10px rgba(0, 0, 0, 0.5);
}
```
-   **First shadow:** `10px` (right), `5px` (down), `15px` (blur), `gray`.
-   **Second shadow:** `inset`, `-5px` (left), `-8px` (up), `10px` (blur), `rgba(0, 0, 0, 0.5)` (semi-transparent black).

---

**5. Write a CSS rule using border-image to apply `border.png` around an image with 30 slice value.**

The `border-image` property requires a border to be set first (usually transparent).

```css
img {
  /* Set a border width for the image to occupy */
  border: 30px solid transparent;

  /* Apply the border-image */
  border-image-source: url('border.png');
  border-image-slice: 30;
  border-image-repeat: stretch; /* or round, repeat */
}
```
This rule tells the browser to use `border.png`, slice it 30px from the edges, and stretch those slices to form the border.

---

**6. Enlist the features of JavaScript.**

Key features of JavaScript include:
-   **High-Level Language:** Abstracts away machine-level complexities.
-   **Dynamically Typed:** Variable types are determined at runtime.
-   **Multi-Paradigm:** Supports object-oriented, functional, and imperative programming styles.
-   **Event-Driven:** Excels at responding to user actions (events) like clicks and key presses.
-   **Prototype-Based Inheritance:** Objects inherit directly from other objects.
-   **First-Class Functions:** Functions are treated like variables (can be passed as arguments, returned from other functions, etc.).

---

**7. Differentiate Let and Var declaration in JavaScript.**

See answer for **Part A, Q.3** in `fat02_2k24_anx.md`. The content is identical.

| Feature | `var` | `let` |
| :--- | :--- | :--- |
| **Scope** | **Function-scoped**. | **Block-scoped**. |
| **Hoisting** | Hoisted and initialized with `undefined`. | Hoisted but not initialized (Temporal Dead Zone). |
| **Re-declaration** | Can be re-declared in the same scope. | Cannot be re-declared in the same scope. |

---

**8. Write a JS function that calculates the factorial of a number using recursion.**

A recursive function is one that calls itself. It must have a base case to stop the recursion.

```javascript
function factorial(n) {
  // Base case: factorial of 0 or 1 is 1
  if (n === 0 || n === 1) {
    return 1;
  }
  // Recursive step: n * factorial of (n-1)
  else {
    return n * factorial(n - 1);
  }
}

// Example usage:
console.log(factorial(5)); // Output: 120
```

---

**9. Given an object `car = { brand: "Toyota", speed: 120}`, add a method `accelerate()` that increases speed by 10 and returns the new speed.**

```javascript
let car = {
  brand: "Toyota",
  speed: 120,
};

// Add the accelerate method to the object
car.accelerate = function() {
  this.speed += 10;
  return this.speed;
};

// Example usage:
console.log(car.accelerate()); // Output: 130
console.log(car.speed);        // Output: 130
```

---

**10. Create an array of 6 random numbers between 1 and 50, sort them in descending order, and display the largest number using the Math object.**

```javascript
// Create an array to hold the random numbers
let randomNumbers = [];

// Generate 6 random numbers between 1 and 50
for (let i = 0; i < 6; i++) {
  // Math.random() gives 0-0.99..., * 50 gives 0-49.99..., + 1 gives 1-50.99..., floor gives 1-50
  const randomNumber = Math.floor(Math.random() * 50) + 1;
  randomNumbers.push(randomNumber);
}

console.log("Generated numbers:", randomNumbers);

// Sort the array in descending order
// The sort compare function (b - a) sorts in descending order
randomNumbers.sort((a, b) => b - a);

console.log("Sorted numbers (descending):", randomNumbers);

// The largest number is now the first element
const largestNumber = randomNumbers[0];

// We can also find the largest number using Math.max with the spread operator
const largestWithMath = Math.max(...randomNumbers);

console.log("Largest number is:", largestNumber);
console.log("Largest number (using Math.max):", largestWithMath);
```

---

## PART B (3 x 10 = 30 Marks)

**11. (a) Explain various types of CSS selectors with examples. How can combining multiple selectors improve the maintainability and specificity of a stylesheet in large-scale web development projects?**

**Types of CSS Selectors:**

1.  **Type Selector (or Element Selector):** Selects all elements of a given type.
    -   **Example:** `p { color: gray; }` (selects all `<p>` elements).

2.  **Class Selector:** Selects all elements with a specific class attribute. It is denoted by a period (`.`).
    -   **Example:** `.highlight { background-color: yellow; }` (selects all elements with `class="highlight"`).

3.  **ID Selector:** Selects a single element with a specific `id` attribute. It is denoted by a hash (`#`). IDs must be unique.
    -   **Example:** `#main-header { font-size: 24px; }` (selects the element with `id="main-header"`).

4.  **Attribute Selector:** Selects elements based on the presence or value of an attribute.
    -   **Example:** `input[type="text"] { border: 1px solid #ccc; }` (selects all text input fields).

5.  **Pseudo-class Selector:** Selects elements based on a certain state. It is denoted by a colon (`:`).
    -   **Example:** `a:hover { text-decoration: underline; }` (selects a link when the mouse is over it).

6.  **Pseudo-element Selector:** Styles a specific part of an element. It is denoted by a double colon (`::`).
    -   **Example:** `p::first-line { font-weight: bold; }` (styles the first line of every paragraph).

**Combinators (Combining Selectors):**

-   **Descendant Selector (space):** Selects elements that are descendants of a specified element.
    -   **Example:** `div p { color: blue; }` (selects all `<p>` elements inside a `<div>`).
-   **Child Selector (`>`):** Selects elements that are direct children of a specified element.
    -   **Example:** `ul > li { list-style-type: none; }` (selects `<li>` elements that are direct children of a `<ul>`).
-   **Adjacent Sibling Selector (`+`):** Selects an element that is immediately preceded by a specified element.
    -   **Example:** `h2 + p { margin-top: 0; }` (selects a `<p>` that comes right after an `<h2>`).

**Improving Maintainability and Specificity:**

Combining selectors is crucial for large-scale projects because it allows for precise targeting without cluttering the HTML with excessive classes.

-   **Maintainability:** By using combinators, you can create styles that are scoped to a specific component. For example, `.user-profile h2` ensures that you are only styling `h2` elements within a user profile component, not all `h2` elements on the site. This makes the CSS modular and easier to maintain.
-   **Specificity:** Specificity is the algorithm browsers use to determine which CSS rule applies if multiple rules target the same element. A more specific selector wins. Combining selectors (e.g., `div#main .content p`) increases specificity, allowing you to override more general styles without using `!important`, which is considered bad practice. This provides fine-grained control in complex stylesheets.

---

**11. (b) Discuss the key features of CSS that make it essential in modern web design. How do these features enhance performance, design consistency, and user experience across web pages?**

CSS (Cascading Style Sheets) is essential in modern web design for several key reasons:

1.  **Separation of Concerns:** CSS allows the separation of a document's content (HTML) from its presentation (style). This is a fundamental principle of modern web development.
    -   **Enhancement:** This separation makes the HTML cleaner and more semantic. It improves **maintainability** because designers can change the entire look of a website by editing only the CSS file, without touching the HTML structure.

2.  **Responsive Web Design (RWD):** Through features like **Media Queries**, CSS allows a single website to adapt its layout to a wide variety of devices and screen sizes.
    -   **Enhancement:** This is critical for **user experience**, ensuring that a site is usable and looks good on desktops, tablets, and mobile phones. It improves **performance** on mobile devices by allowing developers to load smaller images or hide non-essential content.

3.  **Advanced Layout Models (Flexbox and Grid):** CSS Flexbox and Grid provide powerful and flexible tools for creating complex, responsive layouts that were previously very difficult to achieve.
    -   **Enhancement:** These models drastically improve **design consistency** and reduce the need for complex HTML structures or JavaScript hacks for layout, leading to cleaner code and better **performance**.

4.  **Transitions and Animations:** CSS3 introduced native `transition` and `animation` properties.
    -   **Enhancement:** These allow for smooth, visually appealing effects and animations without relying on JavaScript. Because they can be hardware-accelerated by the browser, they offer significantly better **performance** than JavaScript-based animations, leading to a smoother **user experience**.

5.  **Custom Properties (CSS Variables):** This feature allows developers to define reusable values (like colors or spacing) in one place.
    -   **Enhancement:** This greatly improves **design consistency** and **maintainability**. To change a primary brand color across an entire site, you only need to change one variable, ensuring consistency and saving significant development time.

---

**12. (a) Illustrate the ways in which CSS background and text effect properties are combined to improve the design and readability of a webpage? Support your answer with examples of at least five CSS properties.**

CSS background and text properties can be combined to create visually appealing and highly readable designs. A common example is creating a "hero" banner for a webpage.

**Example HTML:**
```html
<div class="hero-banner">
  <h1>Welcome to Our Website</h1>
  <p>Discover amazing things here.</p>
</div>
```

**CSS combining 5+ properties:**
```css
.hero-banner {
  /* 1. background-image: Sets the image */
  background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('hero-image.jpg');
  
  /* 2. background-size: Makes the image cover the area */
  background-size: cover;
  
  /* 3. background-position: Centers the image */
  background-position: center;

  height: 400px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  
  /* 4. color: Sets the text color to white for readability */
  color: white;
  
  /* 5. text-shadow: Adds a subtle shadow to make text pop */
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8);
  
  /* Bonus: text-align for centering */
  text-align: center;
}
```

**Illustration of Improvement:**
1.  **`background-image` with a gradient:** We layer a semi-transparent black `linear-gradient` over the `hero-image.jpg`. This darkens the background image, which is crucial for ensuring that light-colored text placed on top is readable.
2.  **`background-size: cover` and `background-position: center`:** These ensure the background image always looks good, covering the entire banner area without distortion.
3.  **`color: white`:** The white text provides high contrast against the darkened background, which is a key principle of readability.
4.  **`text-shadow`:** The subtle black shadow behind the white text further separates it from the background, dramatically improving readability, especially if the background image has light-colored areas.

By combining these properties, we create a design that is both aesthetically pleasing (a full-width hero image) and highly functional (the text is easy to read).

---

**12. (b) Create a CSS animation for a website button that smoothly changes its background color from blue to green and back repeatedly when hovered over. Describe the CSS properties and keyframes used, and provide the code for the animation.**

To achieve this, we will use a combination of a `@keyframes` animation and the `:hover` pseudo-class to trigger it.

**Description of Properties and Keyframes:**
-   **`@keyframes color-change`**: We will define an animation named `color-change`. It will have three keyframes:
    -   `0%`: The starting state, with a `background-color` of blue.
    -   `50%`: The middle state, with a `background-color` of green.
    -   `100%`: The ending state, returning to a `background-color` of blue to create a smooth loop.
-   **`animation` property:** This shorthand property will be applied to the button on `:hover`.
    -   `animation-name`: `color-change`.
    -   `animation-duration`: How long one cycle takes (e.g., `2s`).
    -   `animation-iteration-count`: `infinite` to make it repeat as long as the user is hovering.
-   **`transition` property:** We'll also add a transition to the base button style to ensure it smoothly returns to its original state when the hover is removed.

**HTML and CSS Code:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Animated Button</title>
    <style>
        /* Define the animation keyframes */
        @keyframes color-change {
            0% { background-color: #007bff; } /* Blue */
            50% { background-color: #28a745; } /* Green */
            100% { background-color: #007bff; } /* Back to Blue */
        }

        .animated-button {
            padding: 15px 30px;
            font-size: 18px;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            background-color: #007bff; /* Initial blue color */
            
            /* Smooth transition for when hover ends */
            transition: background-color 0.5s ease;
        }

        /* Apply the animation when the button is hovered */
        .animated-button:hover {
            animation-name: color-change;
            animation-duration: 2s;
            animation-iteration-count: infinite;
        }
    </style>
</head>
<body>
    <button class="animated-button">Hover Over Me!</button>
</body>
</html>
```

---

**13. (a) Write a JavaScript function named `filterAndTransform` that takes two arguments: an array of numbers and a callback function. The function should filter out all numbers from the array that do not satisfy a condition defined in the callback function and return a new array where the remaining numbers are doubled.**

This function demonstrates the use of higher-order functions and modern array methods (`.filter()` and `.map()`).

```javascript
/**
 * Filters an array of numbers based on a callback condition,
 * then doubles the remaining numbers.
 *
 * @param {number[]} numbersArray - The array of numbers to process.
 * @param {function} filterCallback - A function that takes a number and returns true if it should be kept.
 * @returns {number[]} A new array with the filtered and doubled numbers.
 */
function filterAndTransform(numbersArray, filterCallback) {
  // 1. Filter the array using the provided callback function
  const filteredNumbers = numbersArray.filter(filterCallback);
  
  // 2. Transform (double) the remaining numbers
  const transformedNumbers = filteredNumbers.map(num => num * 2);
  
  // 3. Return the final array
  return transformedNumbers;
}

// --- Example Usage ---

// Example 1: Keep only even numbers
const numbers1 = [1, 2, 3, 4, 5, 6, 7, 8];
const isEven = (num) => num % 2 === 0;
const result1 = filterAndTransform(numbers1, isEven);
console.log(result1); // Output: [4, 8, 12, 16]

// Example 2: Keep only numbers greater than 10
const numbers2 = [5, 10, 15, 20, 25];
const isGreaterThan10 = (num) => num > 10;
const result2 = filterAndTransform(numbers2, isGreaterThan10);
console.log(result2); // Output: [30, 40, 50]
```

---

**13. (b) Elaborate how the Document Object Model (DOM) facilitates dynamic interaction between JavaScript and HTML elements.**

The **Document Object Model (DOM)** is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as a tree of objects, where each node in the tree represents a part of the document (like an element, attribute, or text). JavaScript uses the DOM to facilitate dynamic interaction in several key ways:

1.  **Element Selection:** The DOM provides methods for JavaScript to find and select specific HTML elements. This is the first step to any interaction.
    -   **Methods:** `document.getElementById()`, `document.getElementsByClassName()`, and the modern `document.querySelector()` / `document.querySelectorAll()`.
    -   **Elaboration:** Without these methods, JavaScript would have no way to "grab" a specific button, paragraph, or div to work with.

2.  **Content and Attribute Manipulation:** Once an element is selected, JavaScript can read or change its content and attributes.
    -   **Methods:** `element.innerHTML`, `element.textContent`, `element.setAttribute()`, `element.src`.
    -   **Elaboration:** This allows for dynamic updates without a page reload. For example, displaying a welcome message (`textContent`), showing a new image (`src`), or updating a data table (`innerHTML`).

3.  **Style Manipulation:** JavaScript can dynamically change the CSS styles of an element.
    -   **Methods:** `element.style.property` (e.g., `element.style.color = 'red'`) and `element.classList.add/remove/toggle()`.
    -   **Elaboration:** This is used for visual feedback, like highlighting a selected item, showing/hiding elements (`style.display`), or creating interactive visual effects.

4.  **Event Handling:** The DOM allows JavaScript to listen for user actions (events) on HTML elements.
    -   **Methods:** `element.addEventListener('click', callbackFunction)`.
    -   **Elaboration:** This is the core of interactivity. When a user clicks a button, types in a field, or moves the mouse, JavaScript can "hear" that event and execute a function in response. This is how forms are validated, buttons perform actions, and menus open and close.

5.  **DOM Traversal and Manipulation:** JavaScript can create new elements, delete existing ones, and move them around in the DOM tree.
    -   **Methods:** `document.createElement()`, `parentNode.appendChild()`, `element.remove()`.
    -   **Elaboration:** This is how dynamic lists are populated (e.g., loading search results from an API), notifications are added to the page, and items are removed from a to-do list.

In essence, the DOM acts as the **bridge** between the static HTML document and the dynamic capabilities of JavaScript. JavaScript reads the state of the page through the DOM and writes changes back to the page through the DOM, creating the interactive experience users expect from modern web applications.