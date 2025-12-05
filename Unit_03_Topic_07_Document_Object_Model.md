---
title: "Unit III: Document Object Model (DOM)"
id: unit3-topic7-dom
tags:
  - unit-3
  - javascript
  - dom
  - html-manipulation
  - web-api
alias:
  - "JS DOM"
  - "Document Object Model"
links:
  - "[[UITx/Unit_03_Topic_06_Array_Date_and_Math_Objects.md|Array, Date and Math Objects]]"
  - "[[UITx/Unit_03_Topic_08_Event_Handling.md|Event Handling]]"
---

# Unit III, Topic 7: Document Object Model (DOM)

> [!quote] The web page you see in your browser is not just static text; it is a dynamic, interactive document. The Document Object Model (DOM) is the programming interface that allows JavaScript to interact with this document, transforming it from a passive display into a responsive and engaging user experience. Let us now unlock the power to manipulate the very fabric of our web pages.

## 1. What is the Document Object Model (DOM)?

The **Document Object Model (DOM)** is a programming interface for HTML and XML documents. It represents the page structure as a tree of objects, where each object corresponds to a part of the document (e.g., an element, an attribute, a text node). JavaScript can then use the DOM API to access, change, add, or delete HTML elements and their styles.

Think of the DOM as a structured, object-oriented representation of the web page. When a browser loads an HTML document, it creates a DOM tree.

```
       [Document]
           |
         [html]
         /    \
      [head]  [body]
      /    \  /    \
   [meta] [title] [h1] [p]
                     |    |
                   "Hello" "World"
```

## 2. Accessing HTML Elements (Selecting Elements)

The first step to manipulating the DOM is to select the elements you want to work with.

### a) `document.getElementById(id)`
-   Returns the element that has the ID attribute with the specified value. IDs must be unique.

```javascript
const myDiv = document.getElementById('myDiv');
```

### b) `document.getElementsByClassName(name)`
-   Returns a live HTMLCollection of elements with the specified class name.

```javascript
const paragraphs = document.getElementsByClassName('my-paragraph');
// paragraphs is an array-like object, not a true array
```

### c) `document.getElementsByTagName(name)`
-   Returns a live HTMLCollection of all elements with the specified tag name.

```javascript
const allDivs = document.getElementsByTagName('div');
```

### d) `document.querySelector(selector)` (Modern, Recommended)
-   Returns the first element that matches a specified CSS selector (e.g., `#id`, `.class`, `tag`, `tag.class`).

```javascript
const firstParagraph = document.querySelector('p');
const mySpecificDiv = document.querySelector('#myDiv.special');
```

### e) `document.querySelectorAll(selector)` (Modern, Recommended)
-   Returns a static NodeList of all elements that match a specified CSS selector.

```javascript
const allButtons = document.querySelectorAll('button');
// allButtons is a NodeList, which can be iterated with forEach
```

## 3. Manipulating HTML Elements

Once you have selected an element, you can change its content, attributes, and style.

### a) Changing HTML Content
-   `element.innerHTML`: Gets or sets the HTML content (including tags) of an element.
-   `element.textContent`: Gets or sets the text content of an element (strips out HTML tags).

```html
<p id="demo">Original text.</p>
<div id="container"></div>
```
```javascript
document.getElementById('demo').innerHTML = 'New <strong>bold</strong> text.';
document.getElementById('container').textContent = 'Just plain text.';
```

### b) Changing HTML Attributes
-   `element.attribute = value`: Directly set common attributes.
-   `element.setAttribute(attributeName, value)`: Sets the value of an attribute.
-   `element.getAttribute(attributeName)`: Gets the value of an attribute.
-   `element.removeAttribute(attributeName)`: Removes an attribute.

```html
<img id="myImage" src="old.jpg" alt="Old Image">
```
```javascript
const img = document.getElementById('myImage');
img.src = 'new.jpg'; // Using direct property
img.setAttribute('alt', 'New Image Description'); // Using setAttribute
```

### c) Changing CSS Styles
-   `element.style.property = value`: Directly sets inline CSS styles.

```html
<div id="styledDiv">Hello</div>
```
```javascript
const styledDiv = document.getElementById('styledDiv');
styledDiv.style.backgroundColor = 'red';
styledDiv.style.fontSize = '20px';
```
> [!note] **Best Practice for Styling:**
> While direct `element.style` manipulation works, it's generally better to toggle CSS classes (`element.classList.add()`, `element.classList.remove()`, `element.classList.toggle()`) for more maintainable and organized styling.

## 4. Creating and Deleting Elements

### a) Creating New Elements
-   `document.createElement(tagName)`: Creates a new HTML element.
-   `document.createTextNode(text)`: Creates a new text node.

```javascript
const newDiv = document.createElement('div');
const newText = document.createTextNode('This is a new div.');
newDiv.appendChild(newText); // Add text to the div
```

### b) Appending Elements
-   `parentNode.appendChild(childNode)`: Appends a child node as the last child of a parent node.
-   `parentNode.insertBefore(newNode, referenceNode)`: Inserts a new node before a reference node.

```html
<div id="parent">
    <p>Existing paragraph.</p>
</div>
```
```javascript
const parent = document.getElementById('parent');
const newParagraph = document.createElement('p');
newParagraph.textContent = 'This is a dynamically added paragraph.';
parent.appendChild(newParagraph); // Adds newParagraph after existing paragraph
```

### c) Removing Elements
-   `parentNode.removeChild(childNode)`: Removes a specified child node from the DOM.
-   `childNode.remove()` (Modern, Recommended): Removes the element from its parent.

```javascript
const elementToRemove = document.getElementById('elementToDelete');
elementToRemove.parentNode.removeChild(elementToRemove); // Old way
// OR
elementToRemove.remove(); // New way
```

## 5. Exam-Oriented Insights

DOM manipulation is a core skill for interactive web development.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the Document Object Model (DOM)?**
>     *Answer:* The DOM is a programming interface for HTML and XML documents that represents the page structure as a tree of objects, allowing JavaScript to access and manipulate the document's content, structure, and style.
> 2.  **Name two JavaScript methods used to select HTML elements by their ID or class.**
>     *Answer:* `document.getElementById('id')` and `document.getElementsByClassName('class')` (or `document.querySelector('#id')`, `document.querySelectorAll('.class')`).
> 3.  **How do you change the text content of an HTML element using JavaScript?**
>     *Answer:* By using the `element.textContent` property (to set plain text) or `element.innerHTML` property (to set HTML content).
> 4.  **What is the recommended way to add a new HTML element to the end of an existing parent element using JavaScript?**
>     *Answer:* Using `parentNode.appendChild(childNode)`.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a JavaScript code snippet that selects an element, changes its text content, modifies one of its attributes, and applies a new CSS style. Explain the DOM tree structure with a simple diagram. Discuss the advantages of `querySelector`/`querySelectorAll` over older selection methods. Explain why manipulating `classList` is often preferred over direct `element.style` manipulation for managing element appearance.
```