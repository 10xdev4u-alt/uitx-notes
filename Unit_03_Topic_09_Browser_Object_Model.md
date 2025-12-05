---
title: "Unit III: Browser Object Model (BOM)"
id: unit3-topic9-bom
tags:
  - unit-3
  - javascript
  - bom
  - window-object
  - navigator-object
  - screen-object
  - location-object
  - history-object
aliases:
  - "JS BOM"
  - "Browser Object Model"
links:
  - "[[UITx/Unit_03_Topic_08_Event_Handling.md|Event Handling]]"
  - "[[UITx/Unit_03_Topic_10_Form_Handling_and_Validations.md|Form Handling and Validations]]"
---

# Unit III, Topic 9: Browser Object Model (BOM)

> [!quote] While the DOM allows JavaScript to interact with the content of a web page, the Browser Object Model (BOM) provides the means to interact with the browser window itself and its surrounding environment. It is the gateway to controlling the browser's features, from navigating pages to managing pop-up windows. Let us now explore this broader context of web interaction.

## 1. What is the Browser Object Model (BOM)?

The **Browser Object Model (BOM)** is a collection of browser-specific objects that allow JavaScript to interact with the browser window and its environment. Unlike the DOM, which is a W3C standard, the BOM is not a formal standard, and its objects and methods can vary slightly between different browsers. However, most modern browsers implement a common set of BOM objects.

The top-level object in the BOM hierarchy is the **`window` object**. It represents the browser window and is the global object for all JavaScript code running in the browser. All global variables and functions are properties of the `window` object.

```
       [Window Object]
           |
  +--------+--------+
  |        |        |
[Document] [Navigator] [Screen]
  |        |        |
[HTML DOM] [Location] [History]
```

## 2. Key BOM Objects and Their Properties/Methods

### a) The `window` Object
The `window` object is the global object in client-side JavaScript. It represents the browser window and provides access to all other BOM objects and global functions.

-   **Properties:**
    -   `window.document`: Refers to the `document` object (the DOM).
    -   `window.location`: Refers to the `location` object.
    -   `window.navigator`: Refers to the `navigator` object.
    -   `window.screen`: Refers to the `screen` object.
    -   `window.history`: Refers to the `history` object.
    -   `window.innerWidth`, `window.innerHeight`: The inner width and height of the browser window (viewport).
    -   `window.outerWidth`, `window.outerHeight`: The outer width and height of the browser window (including toolbars/scrollbars).
-   **Methods:**
    -   `window.alert("message")`: Displays an alert box.
    -   `window.confirm("question")`: Displays a confirmation box with OK/Cancel buttons.
    -   `window.prompt("question", "default")`: Displays a dialog box that prompts the user for input.
    -   `window.open("URL", "name", "specs")`: Opens a new browser window or tab.
    -   `window.close()`: Closes the current window.
    -   `window.setTimeout(function, delay)`: Executes a function once after a specified delay.
    -   `window.setInterval(function, delay)`: Executes a function repeatedly with a specified delay between each call.
    -   `window.clearInterval(intervalID)`: Stops a `setInterval` timer.

**Example:**
```javascript
// Get viewport dimensions
console.log(`Viewport width: ${window.innerWidth}px`);

// Open a new tab
// const newTab = window.open('https://www.example.com', '_blank');
```

### b) The `navigator` Object
The `navigator` object contains information about the browser itself.

-   **Properties:**
    -   `navigator.appName`: The name of the browser (deprecated).
    -   `navigator.appVersion`: The version information of the browser.
    -   `navigator.userAgent`: The user-agent header sent by the browser.
    -   `navigator.platform`: The operating system platform.
    -   `navigator.cookieEnabled`: Returns `true` if cookies are enabled.
    -   `navigator.geolocation`: The Geolocation API object (as discussed in Unit 2).
    -   `navigator.onLine`: Returns `true` if the browser is online.

**Example:**
```javascript
console.log(`Browser User-Agent: ${navigator.userAgent}`);
if (navigator.onLine) {
    console.log("You are online!");
} else {
    console.log("You are offline!");
}
```

### c) The `screen` Object
The `screen` object contains information about the user's screen.

-   **Properties:**
    -   `screen.width`, `screen.height`: The total width and height of the user's screen in pixels.
    -   `screen.availWidth`, `screen.availHeight`: The width and height of the screen, excluding permanent user interface features like the Windows Taskbar.
    -   `screen.colorDepth`: The number of bits used to display one color.

**Example:**
```javascript
console.log(`Screen resolution: ${screen.width}x${screen.height}`);
```

### d) The `location` Object
The `location` object contains information about the current URL and allows for navigation.

-   **Properties:**
    -   `location.href`: The entire URL of the current page.
    -   `location.protocol`: The protocol of the URL (e.g., `http:`, `https:`).
    -   `location.host`: The hostname and port number.
    -   `location.hostname`: The hostname (e.g., `www.example.com`).
    -   `location.port`: The port number.
    -   `location.pathname`: The path to the resource (e.g., `/path/to/page.html`).
    -   `location.search`: The query string (e.g., `?param=value`).
    -   `location.hash`: The anchor part of the URL (e.g., `#section1`).
-   **Methods:**
    -   `location.assign("URL")`: Loads a new document.
    -   `location.replace("URL")`: Replaces the current document with a new one (prevents going back with the back button).
    -   `location.reload()`: Reloads the current document.

**Example:**
```javascript
console.log(`Current URL: ${location.href}`);
// location.assign('https://www.newsite.com'); // Navigate to a new page
```

### e) The `history` Object
The `history` object contains the browser's history.

-   **Properties:**
    -   `history.length`: The number of URLs in the history list.
-   **Methods:**
    -   `history.back()`: Loads the previous URL in the history list (same as clicking the browser's back button).
    -   `history.forward()`: Loads the next URL in the history list (same as clicking the browser's forward button).
    -   `history.go(number)`: Loads a specific URL from the history list (e.g., `history.go(-2)` goes back two pages).

**Example:**
```javascript
// history.back(); // Go back one page
```

## 3. Exam-Oriented Insights

The BOM provides essential tools for browser interaction.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the primary function of the Browser Object Model (BOM)?**
>     *Answer:* The BOM allows JavaScript to interact with the browser window itself and its surrounding environment, providing access to browser features like navigation, screen information, and pop-up windows.
> 2.  **Which object is the top-level object in the BOM hierarchy?**
>     *Answer:* The `window` object.
> 3.  **Name two properties of the `window` object that provide information about the browser viewport dimensions.**
>     *Answer:* `window.innerWidth` and `window.innerHeight`.
> 4.  **How would you programmatically navigate the user to the previous page in their browser history using JavaScript?**
>     *Answer:* By calling the `history.back()` method.

> [!tip] **For Higher Mark Questions:**
> Be prepared to differentiate clearly between the DOM and the BOM, explaining their respective scopes and purposes. Provide JavaScript code examples demonstrating the use of `window.setTimeout()`, `window.setInterval()`, and `window.clearInterval()`. Discuss how the `location` object can be used to parse and manipulate parts of the current URL.
