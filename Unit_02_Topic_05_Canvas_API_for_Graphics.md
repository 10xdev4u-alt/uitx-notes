---
title: "Unit II: Designing Graphics using Canvas API"
id: unit2-topic5-canvas-api
tags:
  - unit-2
  - html5
  - canvas
  - javascript
  - graphics
  - 2d-drawing
aliases:
  - "HTML5 Canvas"
links:
  - "[[UITx/Unit_02_Topic_04_Media_Tags.md|Media Tags]]"
  - "[[UITx/Unit_02_Topic_06_Drag_and_Drop_API.md|Drag and Drop API]]"
---

# Unit II, Topic 5: Designing Graphics using Canvas API

> [!quote] The web is not merely a canvas for text and images; it is a canvas for creation itself. The HTML5 Canvas API provides a blank slate and a rich palette of tools, empowering developers to draw, render, and animate graphics directly within the browser using JavaScript. Let us now learn to paint with code.

## 1. What is the Canvas API?

The **HTML5 Canvas API** is a JavaScript API used for drawing graphics on the fly. It provides a `<canvas>` element, which is a container for graphics, and a set of JavaScript functions for drawing shapes, text, images, and other objects onto that container.

The `<canvas>` element itself is just a rectangular area on your page with no drawing content. All drawing is done programmatically using JavaScript. This makes it a powerful tool for data visualization, photo manipulation, real-time video processing, and 2D games.

## 2. Setting Up the Canvas

To use the Canvas API, you first need to add a `<canvas>` element to your HTML document.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Canvas Example</title>
    <style>
        /* Add a border to see the canvas area */
        canvas {
            border: 1px solid black;
        }
    </style>
</head>
<body>
    <h1>My Canvas Drawing</h1>
    <canvas id="myCanvas" width="500" height="300">
        Your browser does not support the HTML5 canvas tag.
    </canvas>
    <script src="drawing.js"></script>
</body>
</html>
```
-   **`id` attribute:** Essential for selecting the canvas element in JavaScript.
-   **`width` and `height` attributes:** Define the size of the drawing surface in pixels.
-   **Fallback Content:** The text inside the `<canvas>` tags is displayed only if the browser does not support the canvas element.

## 3. The Rendering Context

All drawing on the canvas is done through a **rendering context** object. The most common context is the 2D context.

To get the context, you use the `getContext()` method on the canvas element in your JavaScript file (`drawing.js` in this example):

```javascript
// Get the canvas element from the DOM
const canvas = document.getElementById('myCanvas');

// Check if the browser supports canvas
if (canvas.getContext) {
    // Get the 2D rendering context
    const ctx = canvas.getContext('2d');

    // Now you can start drawing on the context (ctx)
}
```

## 4. Drawing Shapes with the 2D Context

The 2D context provides a rich set of methods for drawing.

### a) Rectangles
-   `fillStyle`: Sets the color used to fill shapes.
-   `fillRect(x, y, width, height)`: Draws a filled rectangle.
-   `strokeStyle`: Sets the color used for the outline of shapes.
-   `strokeRect(x, y, width, height)`: Draws a rectangular outline.
-   `clearRect(x, y, width, height)`: Clears the specified rectangular area, making it fully transparent.

**Example:**
```javascript
// Set fill color to blue
ctx.fillStyle = 'blue';
// Draw a filled rectangle at (10, 10) with size 150x75
ctx.fillRect(10, 10, 150, 75);

// Set stroke color to red
ctx.strokeStyle = 'red';
// Draw a rectangular outline at (200, 10) with size 150x75
ctx.strokeRect(200, 10, 150, 75);
```

### b) Paths (Lines, Triangles, Custom Shapes)
Drawing complex shapes involves creating a path.

1.  `beginPath()`: Begins a new path.
2.  `moveTo(x, y)`: Moves the "pen" to a starting point without drawing a line.
3.  `lineTo(x, y)`: Adds a straight line from the current position to the specified point.
4.  `closePath()`: Closes the path by drawing a line from the current point back to the starting point.
5.  `stroke()`: Draws the outline of the path.
6.  `fill()`: Fills the interior of the path.

**Example (drawing a triangle):**
```javascript
ctx.beginPath();
ctx.moveTo(75, 50);    // Start at top-middle
ctx.lineTo(100, 75);   // Draw line to bottom-right
ctx.lineTo(50, 75);    // Draw line to bottom-left
ctx.closePath();       // Close path to form triangle
ctx.strokeStyle = 'green';
ctx.stroke();          // Draw the outline
```

### c) Arcs and Circles
-   `arc(x, y, radius, startAngle, endAngle, counterclockwise)`: Draws an arc or a circle.
    -   Angles are in radians (e.g., `Math.PI * 2` is a full circle).

**Example (drawing a circle):**
```javascript
ctx.beginPath();
ctx.arc(150, 150, 40, 0, Math.PI * 2); // x, y, radius, start, end
ctx.fillStyle = 'orange';
ctx.fill();
```

## 5. Drawing Text and Images

### a) Text
-   `font`: Sets the font properties (e.g., `'30px Arial'`).
-   `fillText(text, x, y)`: Draws filled text.
-   `strokeText(text, x, y)`: Draws outlined text.

**Example:**
```javascript
ctx.font = '30px Arial';
ctx.fillStyle = 'purple';
ctx.fillText('Hello Canvas!', 50, 250);
```

### b) Images
-   `drawImage(image, dx, dy)`: Draws an image onto the canvas. The `image` can be an `<img>` element, another `<canvas>`, or a `<video>` element.

**Example:**
```javascript
const img = new Image();   // Create new img element
img.src = 'myImage.png'; // Set image source
img.onload = function() {
  // Draw the image onto the canvas once it's loaded
  ctx.drawImage(img, 250, 100);
};
```

## 6. Exam-Oriented Insights

The Canvas API is a practical topic that often appears in exams.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the purpose of the HTML5 `<canvas>` element?**
>     *Answer:* The `<canvas>` element provides a container or "drawing surface" in an HTML document. All drawing on it is done programmatically using JavaScript via the Canvas API.
> 2.  **Which JavaScript method is used to get the drawing context of a canvas?**
>     *Answer:* The `getContext()` method, typically called with the argument `'2d'` to get the 2D rendering context (e.g., `canvas.getContext('2d')`).
> 3.  **Name two methods for drawing rectangles on a 2D canvas context.**
>     *Answer:* `fillRect(x, y, width, height)` for drawing a filled rectangle, and `strokeRect(x, y, width, height)` for drawing a rectangular outline.
> 4.  **What is the first step to drawing a custom shape (like a line or triangle) using canvas paths?**
>     *Answer:* The first step is to call the `beginPath()` method to start a new path.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a complete HTML and JavaScript code snippet to draw a simple scene on a canvas (e.g., a house with a roof, a sun). Explain the sequence of path-drawing commands (`beginPath`, `moveTo`, `lineTo`, `closePath`, `stroke`/`fill`). Discuss the difference between the `<canvas>` element and SVG (Scalable Vector Graphics), noting that canvas is a raster-based, immediate-mode API, while SVG is a vector-based, retained-mode API.
