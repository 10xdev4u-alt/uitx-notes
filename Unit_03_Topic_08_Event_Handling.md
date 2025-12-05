---
title: "Unit III: JavaScript Event Handling"
id: unit3-topic8-event-handling
tags:
  - unit-3
  - javascript
  - events
  - event-listeners
  - dom
  - event-propagation
aliases:
  - "JS Events"
links:
  - "[[UITx/Unit_03_Topic_07_Document_Object_Model.md|Document Object Model]]"
  - "[[UITx/Unit_03_Topic_09_Browser_Object_Model.md|Browser Object Model]]"
---

# Unit III, Topic 8: JavaScript Event Handling

> [!quote] The web is a dynamic conversation between the user and the application. Event handling is the mechanism through which JavaScript listens to the user's actions—clicks, key presses, mouse movements—and responds intelligently, transforming a static page into an interactive experience. Let us now master the art of listening and reacting.

## 1. What are Events?

An **event** is something that happens in the HTML document that the browser can respond to. Events are typically triggered by user interaction (e.g., clicking a button, typing in a text field, moving the mouse) or by the browser itself (e.g., page loading, image loading, error occurring).

When an event occurs, JavaScript can detect it and execute specific code in response. This is known as **event handling**.

## 2. Ways to Handle Events

There are several ways to attach event handlers in JavaScript.

### a) Inline Event Handlers (Avoid for best practice)
-   Directly in the HTML tag using an `on<event>` attribute (e.g., `onclick`, `onmouseover`).
-   **Disadvantage:** Mixes HTML and JavaScript, making code harder to maintain and less flexible.

```html
<button onclick="alert('Button clicked!');">Click Me</button>
```

### b) Traditional DOM Event Handlers
-   Assign a function directly to the `on<event>` property of a DOM element.
-   **Disadvantage:** An element can only have one handler per event type. If you assign a second handler, it will overwrite the first.

```html
<button id="myButton">Click Me</button>
<script>
    const button = document.getElementById('myButton');
    button.onclick = function() {
        alert('First handler!');
    };
    button.onclick = function() { // This will overwrite the first one
        alert('Second handler!');
    };
</script>
```

### c) Event Listeners (`addEventListener`) (Recommended)
-   The most flexible and recommended way to handle events.
-   Allows multiple event handlers for the same event type on the same element.
-   Provides more control over event propagation.

`element.addEventListener(event, handler, [options]);`

-   **`event`**: A string representing the event type (e.g., `'click'`, `'mouseover'`, `'keydown'`).
-   **`handler`**: The function to be executed when the event occurs.
-   **`options`**: (Optional) An object that can specify `capture` (boolean), `once` (boolean), `passive` (boolean).

```html
<button id="myButton">Click Me</button>
<script>
    const button = document.getElementById('myButton');

    button.addEventListener('click', function() {
        console.log('Button clicked - Handler 1!');
    });

    button.addEventListener('click', function() { // Both handlers will run
        console.log('Button clicked - Handler 2!');
    });
</script>
```

### Removing Event Listeners (`removeEventListener`)
-   It's good practice to remove event listeners when they are no longer needed, especially in Single Page Applications, to prevent memory leaks.
-   You must pass the *same function reference* that was used to add the listener.

```javascript
function myHandler() {
    console.log('Event handled!');
}
button.addEventListener('click', myHandler);
// ... later ...
button.removeEventListener('click', myHandler);
```

## 3. Common Event Types

-   **Mouse Events:** `click`, `dblclick`, `mousedown`, `mouseup`, `mousemove`, `mouseover`, `mouseout`, `mouseenter`, `mouseleave`.
-   **Keyboard Events:** `keydown`, `keyup`, `keypress`.
-   **Form Events:** `submit`, `change`, `focus`, `blur`, `input`.
-   **Document/Window Events:** `load`, `unload`, `resize`, `scroll`, `DOMContentLoaded`.

## 4. The Event Object

When an event occurs, the event handler function receives an **Event object** as its first argument. This object contains useful information about the event.

### Key Properties of the Event Object:
-   **`event.target`**: The DOM element that triggered the event.
-   **`event.currentTarget`**: The DOM element to which the event listener is currently attached.
-   **`event.type`**: The type of event (e.g., `'click'`).
-   **`event.clientX`, `event.clientY`**: The horizontal and vertical coordinates of the mouse pointer relative to the viewport (for mouse events).
-   **`event.key`, `event.code`**: The key pressed (for keyboard events).

### Key Methods of the Event Object:
-   **`event.preventDefault()`**: Prevents the browser's default action for that event (e.g., preventing a form from submitting, preventing a link from navigating).
-   **`event.stopPropagation()`**: Stops the event from bubbling up the DOM tree to parent elements.

## 5. Event Propagation: Bubbling and Capturing

When an event occurs on an element, it doesn't just fire on that element. It propagates through the DOM tree in two phases:

### a) Capturing Phase (Trickling Down)
-   The event starts from the `window` object, goes down through the document root (`<html>`), `<body>`, and then to the parent elements of the target element, until it reaches the target element itself.
-   Event listeners in this phase are rarely used, but can be specified by setting the third argument of `addEventListener` to `true` or `{ capture: true }`.

### b) Bubbling Phase (Bubbling Up)
-   After reaching the target element, the event "bubbles up" from the target element to its parent, then to its parent's parent, and so on, all the way up to the `window` object.
-   Most event listeners are registered in this phase (default behavior of `addEventListener`).

```
       [Window]
          |
        [Document]
          |
        [html]
          |
        [body]
          |
        [div] (Parent)
          |
        [button] (Target Element)
```
-   **Capturing:** `Window` -> `Document` -> `html` -> `body` -> `div` -> `button`
-   **Bubbling:** `button` -> `div` -> `body` -> `html` -> `Document` -> `Window`

### Event Delegation
-   A technique where you attach a single event listener to a parent element, rather than attaching individual listeners to many child elements.
-   The parent listener then uses `event.target` to identify which child element actually triggered the event.
-   **Benefits:** Improves performance (fewer listeners), simplifies code for dynamically added elements.

```html
<ul id="myList">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```
```javascript
document.getElementById('myList').addEventListener('click', function(event) {
    if (event.target.tagName === 'LI') { // Check if the clicked element is an LI
        console.log('Clicked on:', event.target.textContent);
    }
});
```

## 6. Exam-Oriented Insights

Event handling is fundamental to interactive web applications.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is an event in JavaScript?**
>     *Answer:* An event is something that happens in the HTML document (e.g., user click, page load) that the browser can respond to, allowing JavaScript to execute specific code.
> 2.  **What is the recommended method for attaching event handlers in modern JavaScript?**
>     *Answer:* The `addEventListener()` method.
> 3.  **What is the purpose of `event.preventDefault()`?**
>     *Answer:* It stops the browser's default action for a given event (e.g., preventing a form from submitting or a link from navigating).
> 4.  **Explain the concept of event bubbling.**
>     *Answer:* Event bubbling is the phase of event propagation where an event, after reaching its target element, "bubbles up" through its parent elements in the DOM tree, from the target element up to the `window` object.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write JavaScript code that attaches an event listener to a button, and on click, changes the text content of another element. Explain the advantages of `addEventListener()` over inline or traditional event handlers. Discuss event propagation (capturing and bubbling) and how `event.stopPropagation()` can be used. Provide an example of event delegation and explain its benefits.
