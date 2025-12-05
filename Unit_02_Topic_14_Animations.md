---
title: "Unit II: CSS3 Animations"
id: unit2-topic14-animations
tags:
  - unit-2
  - css3
  - animations
  - keyframes
aliases:
  - "CSS3 Animations"
links:
  - "[[UITx/Unit_02_Topic_13_Transitions.md|Transitions]]"
  - "[[UITx/Unit_02_Quiz.md|Unit 02 Quiz]]"
---

# Unit II, Topic 14: CSS3 Animations

> [!quote] While transitions gracefully guide elements from one state to another, CSS3 Animations allow us to compose entire symphonies of motion. By defining explicit keyframes, we can create complex, multi-step sequences that bring our web pages to life in ways that were once only possible with JavaScript or Flash. Let us now become conductors of this digital orchestra.

## 1. What are CSS Animations?

**CSS Animations** are a powerful feature of CSS3 that allow you to animate the change of CSS properties over time. Unlike transitions, which are limited to a start and an end state, animations can have multiple intermediate steps, defined in a `@keyframes` rule.

Animations give you much finer control over the animation sequence, timing, and repetition.

## 2. The `@keyframes` Rule

The core of a CSS animation is the `@keyframes` at-rule. This is where you define the stages and styles of the animation.

-   You give the animation a name (e.g., `slide-in`, `fade-and-grow`).
-   You define specific points in the animation's timeline using percentages (from `0%` to `100%`) or the keywords `from` (same as `0%`) and `to` (same as `100%`).
-   At each of these points (keyframes), you specify the CSS properties that the element should have.

### Syntax:
```css
@keyframes animation-name {
  from { /* styles for the start of the animation */ }
  50%  { /* styles for the middle of the animation */ }
  to   { /* styles for the end of the animation */ }
}
```

### Example: A Pulsing Glow Animation
```css
@keyframes pulse-glow {
  0% {
    box-shadow: 0 0 5px #ff00de;
  }
  50% {
    box-shadow: 0 0 20px 10px #ff00de;
  }
  100% {
    box-shadow: 0 0 5px #ff00de;
  }
}
```

## 3. Applying the Animation

Once you have defined the `@keyframes`, you apply the animation to an element using the `animation` properties.

### The `animation` Shorthand Property:
`animation: <name> <duration> <timing-function> <delay> <iteration-count> <direction> <fill-mode>;`

-   **`<name>` (required):** The name of the `@keyframes` rule.
-   **`<duration>` (required):** The length of time one cycle of the animation should take.
-   **`<timing-function>`**: The speed curve of the animation (same values as `transition-timing-function`).
-   **`<delay>`**: A delay before the animation starts.
-   **`<iteration-count>`**: How many times the animation should repeat (e.g., `3`, or `infinite` for endless looping).
-   **`<direction>`**: The direction of the animation.
    -   `normal` (default): Plays forward.
    -   `reverse`: Plays backward.
    -   `alternate`: Plays forward then backward.
    -   `alternate-reverse`: Plays backward then forward.
-   **`<fill-mode>`**: Specifies the styles applied to the element before and after the animation runs.
    -   `none` (default): No styles are applied outside the animation time.
    -   `forwards`: Retains the styles from the last keyframe after the animation ends.
    -   `backwards`: Applies the styles from the first keyframe before the animation starts (useful with `animation-delay`).
    -   `both`: Applies both `forwards` and `backwards` rules.

### Example: Applying the `pulse-glow` Animation
```css
.glowing-box {
  width: 100px;
  height: 100px;
  background-color: #333;
  
  /* Apply the animation */
  animation-name: pulse-glow;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

**Shorthand Version:**
```css
.glowing-box {
  width: 100px;
  height: 100px;
  background-color: #333;
  
  /* name duration timing-function iteration-count direction */
  animation: pulse-glow 2s ease-in-out infinite alternate;
}
```

## 4. Longhand Animation Properties

Just like transitions, you can define animation properties individually:
-   `animation-name`
-   `animation-duration`
-   `animation-timing-function`
-   `animation-delay`
-   `animation-iteration-count`
-   `animation-direction`
-   `animation-fill-mode`
-   `animation-play-state`: Allows you to pause (`paused`) and resume (`running`) an animation, often controlled with JavaScript.

## 5. A Complete Animation Example: Sliding and Fading In

#### HTML:
```html
<div class="animated-element">Hello, Animations!</div>
```

#### CSS:
```css
/* Define the keyframes for the animation */
@keyframes slide-and-fade-in {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animated-element {
  padding: 20px;
  background-color: lightcoral;
  color: white;
  
  /* Apply the animation */
  animation: slide-and-fade-in 1.5s ease-out forwards;
}
```
In this example, the element starts with an `opacity` of `0` and is moved `50px` down. Over 1.5 seconds, it fades in (`opacity: 1`) and slides up to its original position (`transform: translateY(0)`). The `forwards` fill mode ensures it stays visible at the end.

## 6. Exam-Oriented Insights

Animations are a powerful tool for creating engaging user experiences.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the purpose of the `@keyframes` rule in CSS3?**
>     *Answer:* The `@keyframes` rule is used to define the stages and styles of a CSS animation, allowing for multi-step sequences by specifying styles at different points in the animation's timeline.
> 2.  **How do you make a CSS animation loop indefinitely?**
>     *Answer:* By setting the `animation-iteration-count` property to `infinite`.
> 3.  **What is the difference between CSS Transitions and CSS Animations?**
>     *Answer:* Transitions are for simple state changes (start to end) and are typically triggered by user interaction. Animations are for complex, multi-step sequences defined with `@keyframes` and can run and loop automatically.
> 4.  **What does `animation-fill-mode: forwards;` do?**
>     *Answer:* It specifies that the element will retain the styles defined in the final keyframe (`100%` or `to`) after the animation has finished playing.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a complete `@keyframes` rule and apply it to an element using the `animation` shorthand property. Explain the different values for `animation-direction` (`normal`, `reverse`, `alternate`). Discuss a practical scenario where you would choose to use a CSS Animation over a CSS Transition, highlighting the advantages of `@keyframes`.
