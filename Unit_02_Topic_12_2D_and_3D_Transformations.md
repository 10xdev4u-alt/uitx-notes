---
title: "Unit II: CSS3 2D and 3D Transformations"
id: unit2-topic12-transformations
tags:
  - unit-2
  - css3
  - transform
  - 2d-transform
  - 3d-transform
  - translate
  - rotate
  - scale
  - skew
aliases:
  - "CSS3 Transformations"
links:
  - "[[UITx/Unit_02_Topic_11_Backgrounds_and_Text_Effects.md|Backgrounds and Text Effects]]"
  - "[[UITx/Unit_02_Topic_13_Transitions.md|Transitions]]"
---

# Unit II, Topic 12: CSS3 2D and 3D Transformations

> [!quote] With CSS3, we can move beyond the flat, two-dimensional plane of the screen. Transformations allow us to manipulate the geometry of an element—to move, rotate, scale, and skew it—without affecting the layout of surrounding elements. This opens a new dimension of visual design and interactivity. Let us now learn to bend and shape our elements.

## 1. What are CSS Transformations?

**CSS Transformations** are a set of properties that let you modify the coordinate space of an element, allowing you to move, rotate, scale, and skew it. These transformations do not affect the document flow, meaning the transformed element does not push other elements around. This makes them ideal for UI effects and animations.

The core property is `transform`, which takes one or more transform functions as its value.

## 2. 2D Transformations

2D transformations operate on the X (horizontal) and Y (vertical) axes.

### a) `translate()`
Moves an element from its current position.
-   `translate(x, y)`: Moves the element by `x` horizontally and `y` vertically.
-   `translateX(x)`: Moves the element horizontally.
-   `translateY(y)`: Moves the element vertically.

**Example:**
```css
.box:hover {
  /* Move 50px to the right and 20px down on hover */
  transform: translate(50px, 20px);
}
```

### b) `rotate()`
Rotates an element around a fixed point (by default, the center of the element).
-   `rotate(angle)`: The angle is specified in degrees (`deg`), radians (`rad`), or turns (`turn`).

**Example:**
```css
.box:hover {
  /* Rotate 45 degrees clockwise on hover */
  transform: rotate(45deg);
}
```

### c) `scale()`
Changes the size of an element.
-   `scale(x, y)`: Scales the element by a factor of `x` horizontally and `y` vertically. A value of `1` is the original size.
-   `scaleX(x)`: Scales horizontally.
-   `scaleY(y)`: Scales vertically.
-   `scale(s)`: Scales both horizontally and vertically by the same factor.

**Example:**
```css
.box:hover {
  /* Make the element 1.5 times larger on hover */
  transform: scale(1.5);
}
```

### d) `skew()`
Skews an element along the X and Y axes.
-   `skew(x-angle, y-angle)`: Skews the element by the given angles.
-   `skewX(angle)`: Skews along the X-axis.
-   `skewY(angle)`: Skews along the Y-axis.

**Example:**
```css
.box:hover {
  /* Skew 20 degrees along the X-axis on hover */
  transform: skewX(20deg);
}
```

### Combining 2D Transformations
You can apply multiple transform functions in a single `transform` property. The order matters!

```css
.box:hover {
  /* Rotate first, then move */
  transform: rotate(45deg) translate(50px);
}
```

## 3. 3D Transformations

3D transformations add the Z-axis, allowing you to create depth and perspective. To enable a 3D space for child elements, the parent container needs the `transform-style: preserve-3d;` and `perspective` properties.

-   **`perspective`**: This property is applied to the *parent* container to give its children a sense of depth. The value determines the intensity of the 3D effect (a lower value means a more extreme perspective).
-   **`transform-style: preserve-3d`**: This is also applied to the parent container to ensure its children are positioned in the 3D space, not flattened onto the parent's plane.

### 3D Transform Functions:
-   `translate3d(x, y, z)` or `translateZ(z)`: Moves an element along the Z-axis (closer to or further from the viewer).
-   `rotate3d(x, y, z, angle)` or `rotateX(angle)`, `rotateY(angle)`, `rotateZ(angle)`: Rotates an element around the specified axis. `rotateZ` is the same as the 2D `rotate`.
-   `scale3d(x, y, z)` or `scaleZ(z)`: Scales an element along the Z-axis.

### Example: A 3D Flipping Card

#### HTML:
```html
<div class="card-container">
  <div class="card">
    <div class="card-front">Front</div>
    <div class="card-back">Back</div>
  </div>
</div>
```

#### CSS:
```css
.card-container {
  width: 200px;
  height: 300px;
  /* Define the perspective for the 3D effect */
  perspective: 1000px;
}

.card {
  width: 100%;
  height: 100%;
  position: relative;
  /* Enable 3D space for children */
  transform-style: preserve-3d;
  transition: transform 0.8s; /* We will cover transitions next */
}

.card-container:hover .card {
  /* Rotate the card on hover */
  transform: rotateY(180deg);
}

.card-front, .card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  /* Hide the back face of the element when it's turned away */
  backface-visibility: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
}

.card-front {
  background-color: lightblue;
}

.card-back {
  background-color: lightcoral;
  /* Position the back face on the other side */
  transform: rotateY(180deg);
}
```

## 4. Other Transform Properties

-   **`transform-origin`**: Changes the position of the origin point (the point around which the transformation occurs). The default is `50% 50%` (the center).
-   **`backface-visibility`**: Specifies whether the back face of an element should be visible when it is facing away from the user.

## 5. Exam-Oriented Insights

Transformations are a visual and practical topic.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the purpose of the CSS `transform` property?**
>     *Answer:* The `transform` property allows you to modify the coordinate space of an element to move, rotate, scale, or skew it without affecting the layout of surrounding elements.
> 2.  **Name two 2D transformation functions.**
>     *Answer:* `translate()`, `rotate()`, `scale()`, `skew()` (any two).
> 3.  **What is the role of the `perspective` property in 3D transformations?**
>     *Answer:* The `perspective` property is applied to a parent container to give its child elements a sense of depth and distance in 3D space.
> 4.  **Does applying a `transform` to an element affect the position of other elements in the document flow?**
>     *Answer:* No, transformations do not affect the document flow. The space taken up by the element remains the same, and other elements are not pushed around.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write CSS code to apply multiple transformations to an element on hover. Explain the difference between `translate()` and using properties like `top`/`left` with `position: relative`. (Hint: `transform` is often more performant as it can be GPU-accelerated). Describe the steps and properties needed to create a 3D "flipping card" effect, explaining the roles of `perspective`, `transform-style`, `backface-visibility`, and `rotateY()`.
