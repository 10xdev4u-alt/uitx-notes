---
title: "Unit II: CSS3 Backgrounds and Text Effects"
id: unit2-topic11-backgrounds-text-effects
tags:
  - unit-2
  - css3
  - backgrounds
  - text-shadow
  - text-effects
  - multiple-backgrounds
aliases:
  - "CSS3 Backgrounds"
  - "CSS3 Text Effects"
links:
  - "[[UITx/Unit_02_Topic_10_Borders_Shadows_and_Fonts.md|Borders, Shadows, and Fonts]]"
  - "[[UITx/Unit_02_Topic_12_2D_and_3D_Transformations.md|2D and 3D Transformations]]"
---

# Unit II, Topic 11: CSS3 Backgrounds and Text Effects

> [!quote] Beyond the shape of boxes and the style of fonts, CSS3 grants us control over the very surface of our elements and the texture of our text. With enhanced backgrounds and advanced text effects, we can create designs with greater depth, richness, and visual interest. Let us master these layers of style.

## 1. Enhanced Background Properties

CSS3 significantly upgraded how we can manipulate the background of an element, introducing properties for more precise control and the ability to layer multiple backgrounds.

### a) `background-size`
This property specifies the size of the background images. Before CSS3, a background image was always its original size.

-   **`auto`**: The default value; the image is displayed in its original size.
-   **`<length>`**: Sets a specific width and height (e.g., `background-size: 100px 50px;`).
-   **`<percentage>`**: Sets the size as a percentage of the parent element.
-   **`cover`**: Resizes the background image to cover the entire container, even if it has to stretch the image or cut a little bit off one of the edges.
-   **`contain`**: Resizes the background image to make sure the image is fully visible, which may leave some empty space in the container.

**Example:**
```css
.hero-section {
  background-image: url('hero.jpg');
  background-repeat: no-repeat;
  /* The image will cover the entire section */
  background-size: cover;
  /* Center the image */
  background-position: center center;
}
```

### b) `background-origin` and `background-clip`
These properties give you finer control over where the background is positioned and painted.

-   **`background-origin`**: Specifies where the `background-position` is relative to.
    -   `padding-box` (default): Position is relative to the padding edge.
    -   `border-box`: Position is relative to the border edge.
    -   `content-box`: Position is relative to the content edge.
-   **`background-clip`**: Specifies the painting area of the background.
    -   `border-box` (default): The background is painted to the outer edge of the border.
    -   `padding-box`: The background is painted to the outer edge of the padding.
    -   `content-box`: The background is painted within the content box.

### c) Multiple Backgrounds
CSS3 allows you to specify multiple background images for an element. Each image can have its own set of background properties. You simply provide comma-separated values for the `background-image` property and other related properties.

**Example:**
```css
.multi-bg {
  background-image: url('foreground.png'), url('background-pattern.png');
  background-repeat: no-repeat, repeat;
  background-position: center, top left;
}
```
The first image in the list is the one on top (closest to the user).

## 2. Advanced Text Effects: `text-shadow`

Similar to `box-shadow`, the `text-shadow` property adds a shadow to text, which can be used to improve readability or for decorative effect.

### Syntax:
`text-shadow: <offset-x> <offset-y> [blur-radius] <color>;`

-   **`<offset-x>` (required):** The horizontal offset of the shadow.
-   **`<offset-y>` (required):** The vertical offset of the shadow.
-   **`[blur-radius]` (optional):** The blur radius.
-   **`<color>` (required):** The color of the shadow.

You can also apply multiple shadows by providing a comma-separated list of shadow values.

### Example:
```css
h1 {
  /* A simple, soft black shadow */
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.neon-text {
  color: #fff;
  /* Multiple shadows to create a neon glow effect */
  text-shadow: 0 0 5px #fff, 
               0 0 10px #fff, 
               0 0 20px #ff00de, 
               0 0 30px #ff00de;
}
```

## 3. Other Text-Related Properties

CSS3 introduced several other properties for handling text overflow and word wrapping.

### a) `text-overflow`
Specifies how to signal to users that there is more content than is visible in the container. It only works when the `overflow` property is set to `hidden`, `scroll`, or `auto`, and `white-space` is `nowrap`.

-   **`clip` (default):** Clips the text.
-   **`ellipsis`**: Renders an ellipsis (`...`) to represent the clipped text.

**Example:**
```css
.truncate {
  width: 200px;
  white-space: nowrap; /* Prevent text from wrapping */
  overflow: hidden;    /* Hide the overflowing text */
  text-overflow: ellipsis;
}
```

### b) `word-wrap` (now `overflow-wrap`)
Allows long words to be broken and wrap onto the next line to prevent overflow.

-   **`normal` (default):** Breaks words only at allowed break points.
-   **`break-word`**: Allows unbreakable words to be broken.

### c) `word-break`
Specifies how words should break when reaching the end of a line.

-   **`normal`**: Default break rule.
-   **`break-all`**: Allows breaks between any two characters (useful for non-ideographic languages).
-   **`keep-all`**: Prevents breaks for CJK (Chinese, Japanese, Korean) text.

## 4. Exam-Oriented Insights

Backgrounds and text effects are common styling tasks.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the purpose of the `background-size: cover;` declaration?**
>     *Answer:* It scales the background image to be as large as possible to completely cover the container, even if it means cropping the image.
> 2.  **How can you apply multiple background images to a single element in CSS3?**
>     *Answer:* By providing a comma-separated list of URLs in the `background-image` property, along with corresponding comma-separated values for other background properties.
> 3.  **What does the `text-shadow` property do?**
>     *Answer:* It adds a shadow effect to text, which can be configured with horizontal and vertical offsets, a blur radius, and a color.
> 4.  **Which CSS property is used to display an ellipsis (...) for overflowing text?**
>     *Answer:* The `text-overflow: ellipsis;` property, used in conjunction with `overflow: hidden;` and `white-space: nowrap;`.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write CSS code to create a full-width hero banner with a background image that covers the entire area. Explain the difference between `background-size: cover` and `background-size: contain`. Demonstrate how to create a "neon glow" effect on text using multiple `text-shadow` values. Explain the conditions required for `text-overflow: ellipsis` to work correctly.
