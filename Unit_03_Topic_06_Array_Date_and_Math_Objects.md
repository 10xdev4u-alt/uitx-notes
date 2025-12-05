---
title: "Unit III: JavaScript Array, Date, and Math Objects"
id: unit3-topic6-array-date-math-objects
tags:
  - unit-3
  - javascript
  - arrays
  - date-object
  - math-object
  - built-in-objects
aliases:
  - "JS Arrays"
  - "JS Date"
  - "JS Math"
links:
  - "[[UITx/Unit_03_Topic_05_Objects.md|Objects]]"
  - "[[UITx/Unit_03_Topic_07_Document_Object_Model.md|Document Object Model]]"
---

# Unit III, Topic 6: JavaScript Array, Date, and Math Objects

> [!quote] Beyond simple variables and custom objects, JavaScript provides powerful built-in objects to handle common programming tasks: managing ordered collections of data, working with time, and performing mathematical operations. These objects are indispensable tools in a developer's arsenal. Let us now master their utility.

## 1. The `Array` Object: Ordered Collections

An **Array** is a special type of object used to store ordered collections of data. Unlike objects, which use named keys, arrays use numerical indices (starting from 0) to access their elements.

### a) Creating Arrays
-   **Array Literal (Most Common):**
    ```javascript
    const fruits = ["Apple", "Banana", "Cherry"];
    const numbers = [1, 2, 3, 4, 5];
    ```
-   **`new Array()` Constructor:**
    ```javascript
    const cars = new Array("Ford", "BMW", "Audi");
    const emptyArray = new Array(5); // Creates an array with 5 empty slots
    ```

### b) Accessing and Modifying Elements
Elements are accessed using their zero-based index.

```javascript
console.log(fruits[0]); // Output: Apple
fruits[1] = "Orange";   // Modify an element
console.log(fruits);    // Output: ["Apple", "Orange", "Cherry"]
```

### c) Array Properties and Methods
Arrays come with a rich set of built-in properties and methods.

-   **`length` property:** Returns the number of elements in the array.
    ```javascript
    console.log(fruits.length); // Output: 3
    ```
-   **`push()`:** Adds one or more elements to the end of an array and returns the new length.
-   **`pop()`:** Removes the last element from an array and returns that element.
-   **`unshift()`:** Adds one or more elements to the beginning of an array.
-   **`shift()`:** Removes the first element from an array and returns that element.
-   **`indexOf()`:** Returns the first index at which a given element can be found in the array, or -1 if it is not present.
-   **`includes()` (ES6+):** Checks if an array includes a certain value among its entries, returning `true` or `false`.
-   **`slice(start, end)`:** Returns a shallow copy of a portion of an array into a new array object.
-   **`splice(start, deleteCount, item1, ...)`:** Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.
-   **`forEach(callback)`:** Executes a provided function once for each array element.
-   **`map(callback)`:** Creates a new array populated with the results of calling a provided function on every element in the calling array.
-   **`filter(callback)`:** Creates a new array with all elements that pass the test implemented by the provided function.
-   **`reduce(callback, initialValue)`:** Executes a reducer function on each element of the array, resulting in a single output value.

**Example `map`:**
```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6]
```

## 2. The `Date` Object: Working with Time

The **`Date` object** is used to work with dates and times. It allows you to create, manipulate, and format dates.

### a) Creating Date Objects
-   **`new Date()`:** Creates a new Date object with the current date and time.
-   **`new Date(year, month, day, hours, minutes, seconds, milliseconds)`:** Creates a Date object with specified values (month is 0-indexed: 0 for January, 11 for December).
-   **`new Date(milliseconds)`:** Creates a Date object from a timestamp (milliseconds since January 1, 1970, UTC).
-   **`new Date(dateString)`:** Creates a Date object from a date string.

**Example:**
```javascript
const now = new Date();
console.log(now); // Output: Current date and time

const christmas2025 = new Date(2025, 11, 25); // Month 11 is December
console.log(christmas2025);
```

### b) Date Methods
The `Date` object has many methods for getting and setting parts of a date.

-   **`getFullYear()`:** Gets the year (4 digits).
-   **`getMonth()`:** Gets the month (0-11).
-   **`getDate()`:** Gets the day of the month (1-31).
-   **`getHours()`:** Gets the hour (0-23).
-   **`getMinutes()`:** Gets the minutes (0-59).
-   **`getSeconds()`:** Gets the seconds (0-59).
-   **`getDay()`:** Gets the day of the week (0 for Sunday, 6 for Saturday).
-   **`getTime()`:** Gets the number of milliseconds since January 1, 1970, UTC.
-   **`setFullYear()`, `setMonth()`, etc.:** Methods to set date components.
-   **`toDateString()`:** Returns the date portion of a Date object as a human-readable string.
-   **`toLocaleDateString()`, `toLocaleTimeString()`:** Returns date/time strings formatted according to the user's locale.

**Example:**
```javascript
const d = new Date();
console.log(`Today is ${d.toLocaleDateString()} and the time is ${d.toLocaleTimeString()}.`);
```

## 3. The `Math` Object: Mathematical Operations

The **`Math` object** is a built-in object that has properties and methods for mathematical constants and functions. It is not a constructor; all its properties and methods are static.

### a) Math Properties
-   **`Math.PI`**: The ratio of a circle's circumference to its diameter (approximately 3.14159).
-   **`Math.E`**: Euler's number (approximately 2.718).

### b) Math Methods
-   **`Math.round(x)`:** Rounds `x` to the nearest integer.
-   **`Math.floor(x)`:** Rounds `x` down to the nearest integer.
-   **`Math.ceil(x)`:** Rounds `x` up to the nearest integer.
-   **`Math.random()`:** Returns a pseudo-random floating-point number between 0 (inclusive) and 1 (exclusive).
-   **`Math.max(x, y, ...)`:** Returns the largest of zero or more numbers.
-   **`Math.min(x, y, ...)`:** Returns the smallest of zero or more numbers.
-   **`Math.pow(x, y)`:** Returns `x` to the power of `y`.
-   **`Math.sqrt(x)`:** Returns the square root of `x`.
-   **`Math.abs(x)`:** Returns the absolute value of `x`.

**Example:**
```javascript
console.log(Math.PI);           // 3.141592653589793
console.log(Math.round(4.7));   // 5
console.log(Math.floor(4.7));   // 4
console.log(Math.random());     // A random number between 0 and 1
console.log(Math.max(10, 20, 5)); // 20
```

## 4. Exam-Oriented Insights

These built-in objects are frequently used in practical JavaScript development.

> [!question] **Potential 2-Mark Questions:**
> 1.  **How do you create an empty array with 5 predefined empty slots in JavaScript?**
>     *Answer:* Using the `new Array()` constructor: `const arr = new Array(5);`.
> 2.  **Which array method adds an element to the end of an array?**
>     *Answer:* The `push()` method.
> 3.  **What is the significance of the month parameter in the `new Date(year, month, ...)` constructor?**
>     *Answer:* The month parameter is zero-indexed, meaning 0 represents January, 1 represents February, and so on, up to 11 for December.
> 4.  **Which `Math` object method is used to generate a random number between 0 (inclusive) and 1 (exclusive)?**
>     *Answer:* `Math.random()`.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write JavaScript code to perform common array manipulations (e.g., adding/removing elements, iterating, mapping). Demonstrate how to create a `Date` object for a specific future date and extract its year, month, and day. Explain how to generate a random integer within a specific range using `Math.random()` and `Math.floor()`. Discuss the difference between `slice()` and `splice()` for array manipulation.
