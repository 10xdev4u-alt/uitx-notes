---
title: "Unit II: CSS3 Borders, Shadows, and Fonts"
id: unit2-topic10-borders-shadows-fonts
tags:
  - unit-2
  - css3
  - border-radius
  - box-shadow
  - border-image
  - web-fonts
  - font-face
aliases:
  - "CSS3 Borders"
  - "CSS3 Shadows"
  - "CSS3 Web Fonts"
links:
  - "[[UITx/Unit_02_Topic_09_Intro_to_CSS3_and_Features.md|Introduction to CSS3 and its Features]]"
  - "[[UITx/Unit_02_Topic_11_Backgrounds_and_Text_Effects.md|Backgrounds and Text Effects]]"
---

# Unit II, Topic 10: CSS3 Borders, Shadows, and Fonts

> [!quote] The artistry of web design lies in the details: the gentle curve of a container, the subtle shadow that lifts it from the page, and the unique character of its typography. CSS3 provides the tools to master these details, transforming simple boxes and text into elegant design elements. Let us explore these foundational styling features.

## 1. `border-radius`: Creating Rounded Corners

One of the most celebrated features of CSS3, `border-radius` allows developers to easily create rounded corners on elements, a task that previously required slicing images or using complex `div` structures.

### Syntax:
You can specify one, two, three, or four values.
-   **One value:** Applies to all four corners. `border-radius: 10px;`
-   **Two values:** First value for top-left/bottom-right, second for top-right/bottom-left. `border-radius: 10px 20px;`
-   **Three values:** First for top-left, second for top-right/bottom-left, third for bottom-right. `border-radius: 10px 20px 30px;`
-   **Four values:** Applies to top-left, top-right, bottom-right, bottom-left in that order. `border-radius: 10px 20px 30px 40px;`

To create a perfect circle from a square element, set the `border-radius` to `50%`.

### Example:
```css
.box {
  width: 200px;
  height: 100px;
  border: 2px solid #333;
  background-color: lightblue;
  /* Applies a 15px radius to all corners */
  border-radius: 15px;
}

.circle {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  /* Creates a circle */
  border-radius: 50%;
}
```

## 2. `box-shadow`: Adding Depth with Shadows

The `box-shadow` property adds shadow effects around an element's frame. You can specify multiple shadows, separated by commas.

### Syntax:
`box-shadow: [inset] <offset-x> <offset-y> [blur-radius] [spread-radius] <color>;`

-   **`inset` (optional):** If present, changes the shadow from an outer shadow (default) to an inner shadow.
-   **`<offset-x>` (required):** The horizontal offset of the shadow. A positive value puts it to the right of the box, a negative value to the left.
-   **`<offset-y>` (required):** The vertical offset. A positive value puts it below the box, a negative value above.
-   **`[blur-radius]` (optional):** The blur radius. The larger the value, the more blurred the shadow becomes.
-   **`[spread-radius]` (optional):** The spread radius. A positive value expands the shadow, a negative value shrinks it.
-   **`<color>` (required):** The color of the shadow.

### Example:
```css
.shadow-box {
  width: 200px;
  height: 100px;
  background-color: white;
  /* A subtle, blurred shadow */
  box-shadow: 5px 5px 15px 5px rgba(0, 0, 0, 0.2);
}

.inset-shadow-box {
  width: 200px;
  height: 100px;
  background-color: #eee;
  /* An inner shadow to give a "pressed" look */
  box-shadow: inset 2px 2px 5px rgba(0, 0, 0, 0.3);
}
```

## 3. `border-image`: Using Images for Borders

The `border-image` property allows you to specify an image to be used as the border around an element, instead of a solid color. This is a more advanced property for creating highly stylized designs.

### Syntax:
`border-image: <source> <slice> [width] [outset] <repeat>;`

-   **`<source>`**: The URL of the image to use for the border (`url('border.png')`).
-   **`<slice>`**: Specifies how to slice the image into 9 sections (corners, edges, and center).
-   **`<repeat>`**: Defines how the edge regions of the source image are adjusted to fit the dimensions of the border image (`stretch`, `repeat`, `round`).

### Example:
```css
#fancy-border {
  border: 30px solid transparent;
  padding: 15px;
  /* Use 'border.png' as the border, slicing it at 30px from each edge */
  border-image: url('border.png') 30 stretch;
}
```
This property is powerful but can be complex to master. It's most useful for decorative, non-rectangular border designs.

## 4. `@font-face`: Custom Web Fonts

Perhaps one of the most transformative features for web typography, the `@font-face` rule allows you to use custom fonts on your website. The browser downloads the font file along with other assets like images and CSS.

### Syntax:
You define the font family name and point to the font file(s).

```css
@font-face {
  font-family: 'MyCustomFont'; /* The name you will use to refer to this font */
  src: url('mycustomfont.woff2') format('woff2'), /* Modern format */
       url('mycustomfont.woff') format('woff');   /* Older format */
  font-weight: normal;
  font-style: normal;
}
```
-   **`font-family`**: Defines the name for the font.
-   **`src`**: Specifies the path to the font file. It's best practice to provide multiple formats for cross-browser compatibility. `woff2` is the modern standard.
-   **`format()`**: Helps the browser identify the font format.

### Using the Custom Font:
Once defined, you can use the font family name just like any other font in your CSS.

```css
body {
  font-family: 'MyCustomFont', Arial, sans-serif; /* Use custom font, with fallbacks */
}

h1 {
  font-family: 'MyCustomFont', serif;
}
```
-   **Font Services:** Services like Google Fonts and Adobe Fonts simplify this process by hosting the fonts and providing the necessary `@font-face` CSS for you.

## 5. Exam-Oriented Insights

These properties are fundamental to modern CSS styling.

> [!question] **Potential 2-Mark Questions:**
> 1.  **How do you create a perfect circle using CSS on a square element?**
>     *Answer:* By setting the `border-radius` property to `50%`.
> 2.  **What are the two required values for the `box-shadow` property?**
>     *Answer:* The horizontal offset (`offset-x`) and the vertical offset (`offset-y`).
> 3.  **What is the purpose of the `@font-face` rule in CSS3?**
>     *Answer:* It allows developers to define and use custom fonts on a website, which are downloaded by the browser, enabling richer typography.
> 4.  **Briefly describe what the `border-image` property does.**
>     *Answer:* The `border-image` property allows you to use an image as the border of an element, replacing the standard solid-color border.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write CSS code to demonstrate a combination of these properties (e.g., a box with rounded corners and a drop shadow). Explain the different values of the `box-shadow` property (x-offset, y-offset, blur, spread, color, inset). Discuss the importance of providing multiple font formats in an `@font-face` rule for cross-browser compatibility.
