---
title: "Unit II: CSS3 Transitions"
id: unit2-topic13-transitions
tags:
  - unit-2
  - css3
  - transitions
  - animation
  - timing-functions
aliases:
  - "CSS3 Transitions"
links:
  - "[[UITx/Unit_02_Topic_12_2D_and_3D_Transformations.md|2D and 3D Transformations]]"
  - "[[UITx/Unit_02_Topic_14_Animations.md|Animations]]"
---

# Unit II, Topic 13: CSS3 Transitions

> [!quote] Transformations change properties instantly, but true elegance in motion is found in gradual change. CSS3 Transitions are the bridge between states, allowing property changes to occur smoothly over a specified duration. They are the key to creating fluid, natural-feeling user interfaces. Let us now learn to control the flow of time.

## 1. What are CSS Transitions?

**CSS Transitions** provide a way to control the speed of an animation when changing CSS properties. Instead of property changes taking effect immediately, you can cause the changes to occur over a period of time.

For example, if you change the `background-color` of an element, it normally changes instantly. With transitions, you can make that color change fade in smoothly over half a second.

Transitions are typically triggered by pseudo-classes like `:hover`, `:focus`, or by dynamically adding/removing classes with JavaScript.

## 2. The `transition` Shorthand Property

The easiest way to define a transition is with the `transition` shorthand property.

### Syntax:
`transition: <property> <duration> <timing-function> <delay>;`

-   **`<property>` (required):** The name of the CSS property to apply the transition to (e.g., `background-color`, `width`, `transform`). You can also use the value `all` to apply the transition to all changeable properties.
-   **`<duration>` (required):** The length of time the transition should take (e.g., `1s`, `500ms`).
-   **`<timing-function>` (optional):** Controls the speed curve of the transition.
-   **`<delay>` (optional):** Specifies a delay before the transition starts.

**Example:**
```css
.button {
  background-color: blue;
  color: white;
  padding: 10px 20px;
  border-radius: 5px;
  /* Apply a transition to the background-color property,
     taking 0.5 seconds, with an ease-in-out timing function. */
  transition: background-color 0.5s ease-in-out;
}

.button:hover {
  background-color: darkblue;
}
```
In this example, when the user hovers over the button, the background color will smoothly fade from `blue` to `darkblue` over 0.5 seconds.

## 3. The Longhand Transition Properties

You can also define transitions using their individual properties.

### a) `transition-property`
Specifies the name of the CSS property the transition effect is for.
`transition-property: width;`
`transition-property: all;`
`transition-property: background-color, transform;` (for multiple properties)

### b) `transition-duration`
Specifies how many seconds or milliseconds a transition animation should take to complete.
`transition-duration: 2s;`

### c) `transition-timing-function`
This property controls the acceleration curve of the transition, defining how the property changes over its duration.

-   **`ease` (default):** Slow start, then fast, then end slowly.
-   **`linear`**: Same speed from start to end.
-   **`ease-in`**: Slow start.
-   **`ease-out`**: Slow end.
-   **`ease-in-out`**: Slow start and end (similar to `ease` but more symmetrical).
-   **`cubic-bezier(n,n,n,n)`**: Allows you to define your own custom timing function.

### d) `transition-delay`
Specifies a delay (in seconds or milliseconds) for the start of the transition effect.
`transition-delay: 1s;`

## 4. Transitioning Multiple Properties

You can transition multiple properties at once by providing a comma-separated list.

**Shorthand Example:**
```css
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  transform: rotate(0deg);
  transition: width 1s linear, 
              background-color 0.5s ease-in, 
              transform 1s ease-out;
}

.box:hover {
  width: 200px;
  background-color: orange;
  transform: rotate(90deg);
}
```
In this example:
-   The `width` will change over 1 second with a `linear` timing.
-   The `background-color` will change over 0.5 seconds with an `ease-in` timing.
-   The `transform` will change over 1 second with an `ease-out` timing.

## 5. Transitions vs. Animations

While both create motion, they serve different purposes.

-   **Transitions:** Designed for simple state changes. They have a starting state and an ending state. They are perfect for simple interactions like hover effects.
-   **Animations (`@keyframes`):** Designed for more complex, multi-step sequences. They can have multiple keyframes (intermediate steps) and can loop indefinitely without user interaction. We will cover animations in the next topic.

## 6. Exam-Oriented Insights

Transitions are fundamental to modern, interactive UI design.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the purpose of CSS Transitions?**
>     *Answer:* CSS Transitions allow property changes in CSS to occur smoothly over a specified duration, rather than happening instantly, which is used to create simple animations and effects.
> 2.  **What are the two required properties when defining a transition?**
>     *Answer:* `transition-property` (which property to animate) and `transition-duration` (how long the animation should take).
> 3.  **What does the `transition-timing-function: ease-in-out;` do?**
>     *Answer:* It specifies that the transition will start slowly, speed up in the middle, and then end slowly, creating a more natural-feeling motion.
> 4.  **How do you apply a transition effect to all changeable properties of an element?**
>     *Answer:* By using the value `all` for the `transition-property` (e.g., `transition: all 0.5s ease;`).

> [!tip] **For Higher Mark Questions:**
> Be prepared to write CSS code to create a hover effect that smoothly changes multiple properties (e.g., size, color, and rotation) of an element. Explain the difference between the various `transition-timing-function` values (`ease`, `linear`, `ease-in`, `ease-out`). Differentiate between CSS Transitions and CSS Animations, explaining when you would choose to use one over the other.
