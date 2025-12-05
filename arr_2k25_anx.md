---
title: "End Semester Exam - QP-2 2025 - Answer Key"
id: arr-2k25-anx
tags:
  - semester-exam
  - answers
  - unit-1
  - unit-2
  - unit-3
  - unit-4
  - unit-5
aliases:
  - "ARR 2025 Answers"
links:
  - "[[UITx/arr_2k25.md|Arrear 2025 Question Paper]]"
---

# CS22503A – User Interface Tools and Techniques
## End Semester Examination - Answer Key (Dec 2024)

> [!note] This document provides detailed answers for the End Semester Examination (QP-2) paper.

---

## PART- A (20 x 2 = 40 Marks)

**1. State the purpose of SMTP in networking.**

The purpose of **SMTP (Simple Mail Transfer Protocol)** is to **send and transfer email messages** across the internet. It operates on a "push" model, pushing emails from a client to a server, and then from the sender's mail server to the recipient's mail server.

---

**2. Differentiate HTTP from HTTPS.**

| Feature | HTTP (HyperText Transfer Protocol) | HTTPS (HyperText Transfer Protocol Secure) |
| :--- | :--- | :--- |
| **Security** | Transmits data in plain text, making it insecure and vulnerable to eavesdropping. | Encrypts data using SSL/TLS, ensuring privacy, integrity, and authentication. |
| **Port** | Uses port 80 by default. | Uses port 443 by default. |
| **URL Scheme** | URL begins with `http://`. | URL begins with `https://`. |

In essence, HTTPS is the secure version of HTTP.

---

**3. List the different types of web pages.**

There are two primary types of web pages:
1.  **Static Web Pages:** These have fixed content that is delivered to the user exactly as it is stored on the server. The content does not change unless the HTML file itself is manually updated.
2.  **Dynamic Web Pages:** The content is generated on-the-fly by the server at the time of the request, often based on user input or data from a database. This allows for personalized and interactive content.

---

**4. Elucidate the significance of dynamic web pages.**

The significance of dynamic web pages lies in their ability to create **interactive, personalized, and real-time user experiences**. Unlike static pages, they can:
-   Display content based on user identity (e.g., a personalized welcome message).
-   Allow user interaction (e.g., submitting forms, posting comments).
-   Fetch and display real-time data from a database (e.g., e-commerce product listings, social media feeds).

---

**5. Assess the importance of Geolocation API in modern web development.**

The Geolocation API is important because it allows web applications to access a user's geographical location (with their permission). This enables a wide range of **location-based services**, such as:
-   Displaying maps and providing navigation.
-   Suggesting nearby points of interest ("restaurants near me").
-   Tagging social media posts with a location.

---

**6. Justify the use of web storage (local and session storage) over cookies.**

Web storage is justified over cookies for client-side data storage for two main reasons:
1.  **Larger Storage Capacity:** Web storage provides a much larger capacity (5-10MB) compared to cookies (4KB), allowing for storage of more complex data.
2.  **Reduced Network Overhead:** Web storage data is not automatically sent with every HTTP request, unlike cookies. This reduces network traffic and improves application performance.

---

**7. Enlist the advanced text effects supported by CSS3.**

CSS3 supports several advanced text effects, including:
-   **`text-shadow`:** Adds a shadow behind text, which can be used for depth or glow effects.
-   **`text-overflow`:** Specifies how to signal clipped text to the user, typically with an ellipsis (`...`).
-   **`word-wrap` / `overflow-wrap`:** Allows long words to be broken to prevent layout overflow.
-   **`@font-face`:** Allows the use of custom fonts (web fonts).

---

**8. Define semantic tags and their importance in HTML5.**

**Semantic tags** are HTML elements that clearly describe their meaning and the type of content they hold to both the browser and the developer.
-   **Importance:**
    1.  **Accessibility:** They help screen readers interpret the page structure, making the site more accessible to visually impaired users.
    2.  **SEO:** They provide context to search engines, helping them better understand and rank the content.
    3.  **Maintainability:** They make the code more readable and easier to maintain.
-   **Examples:** `<header>`, `<nav>`, `<article>`, `<footer>`.

---

**9. Classify the variable types available in JavaScript.**

JavaScript data types can be classified into two main categories:
1.  **Primitive Types:** These are immutable data types.
    -   `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`.
2.  **Complex (or Reference) Type:**
    -   `object`: A collection of properties. This includes plain objects, arrays, functions, and other built-in objects like `Date`.

---

**10. Compare XML and JSON in terms of data representation.**

| Feature | XML (eXtensible Markup Language) | JSON (JavaScript Object Notation) |
| :--- | :--- | :--- |
| **Structure** | Uses tags with opening and closing pairs to define elements in a tree structure. | Uses key-value pairs (like JavaScript object literals) and arrays. |
| **Verbosity** | More verbose due to closing tags and tag-based structure. | Less verbose, more compact, and generally easier for humans to read. |
| **Example** | `<person><name>John</name></person>` | `{"name": "John"}` |

---

**11. Sketch the structure of a simple AJAX request.**

AJAX allows a web page to communicate with a server asynchronously without a full page reload.

**Sketch of the Flow:**
```
+-----------------+       +-----------------+       +-----------------+
|   Web Browser   |       |   The Internet  |       |   Web Server    |
| (JavaScript)    |       |                 |       |                 |
+-----------------+       +-----------------+       +-----------------+
        |                                                     |
1. User Event (e.g., click)                                   |
        |                                                     |
        |---- 2. Create XHR Object & Send Async Request ----> |
        |                                                     |
        |                                       3. Process Request &
        |                                          Prepare Response
        |                                                     |
        |<--- 4. Receive Response Data (JSON/XML) ----------- |
        |                                                     |
5. Update Page Content (DOM Manipulation)                     |
        |                                                     |
```

---

**12. What are the various control statements in JavaScript?**

See answer for **Part A, Q.7** in `fat02_2k24_anx.md`.

---

**13. Interpret the various types of web design in HCI.**

In HCI, web design approaches focus on how a site adapts to different devices:
1.  **Fixed Design:** The layout has a fixed width and does not change with the screen size. This is an outdated approach.
2.  **Fluid Design:** The layout uses percentage-based widths, so it stretches or shrinks to fit the browser window.
3.  **Adaptive Design:** The design has several predefined fixed layouts. The server or client-side script detects the screen size and serves the most appropriate layout.
4.  **Responsive Design (Most Common):** A combination of fluid grids and CSS media queries that allows the design to fluidly adapt to any screen size, re-arranging content as needed.

---

**14. Justify the need for designing user-friendly systems in HCI.**

Designing user-friendly systems is essential because:
-   **It Increases Efficiency and Productivity:** Users can complete tasks faster and with less effort.
-   **It Reduces Errors:** An intuitive interface minimizes user mistakes, which is critical in many applications.
-   **It Improves User Satisfaction and Adoption:** Users are more likely to use and recommend a product that is easy and pleasant to use.
-   **It Reduces Training and Support Costs:** If a system is easy to learn, it requires less training and fewer support calls.

---

**15. What is meant by web scraping, and why is it used?**

See answer for **Part A, Q.13** in `sem_2k24_anx.md`.

---

**16. Enlist the programming languages commonly used for web scraping.**

See answer for **Part A, Q.1** in `fat03_2k25_anx.md`.

---

**17. Define Node.js and its primary use.**

**Node.js** is an open-source, back-end JavaScript runtime environment that executes JavaScript code outside of a web browser.
-   **Primary Use:** Its primary use is for building fast, scalable, and data-intensive **network applications**, such as web servers, APIs, and real-time applications (e.g., chat servers).

---

**18. Specify the steps involved in setting up a Node.js server.**

The basic code steps to set up a Node.js server using the `http` module are:
1.  **Import `http` module:** `const http = require('http');`
2.  **Create Server:** Use `http.createServer()` and provide a callback function to handle requests and responses.
3.  **Send Response:** Inside the callback, use `res.writeHead()` to set headers and `res.end()` to send content and close the connection.
4.  **Start Listening:** Call `server.listen(port, hostname, callback)` to make the server start listening for incoming requests.

---

**19. Construct an example of a POST request in Node.js.**

This example shows how a Node.js server handles an incoming POST request by collecting the data from the request body stream.

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  if (req.method === 'POST' && req.url === '/data') {
    let body = '';
    // Listen for data chunks
    req.on('data', chunk => {
      body += chunk.toString();
    });
    // When all data is received
    req.on('end', () => {
      console.log('Received data:', body);
      res.end('Data received successfully.');
    });
  }
});
```

---

**20. Infer the importance of connecting a NoSQL database using Node.js.**

Connecting a NoSQL database (like MongoDB) to Node.js is important because:
1.  **Data Format Synergy:** NoSQL databases like MongoDB use JSON-like documents (BSON), which map naturally to JavaScript objects, making data manipulation seamless and intuitive in Node.js.
2.  **Scalability:** Both Node.js and NoSQL databases are designed for high scalability, making them a powerful combination for modern applications that need to handle large volumes of data and concurrent users.

---

## PART- B (5 x 10 = 50 Marks)

**21. (a) Model the architecture of the WWW and explain its components in detail.**

See answer for **Part B, Q.12(a)** in `fat01_2k25_anx.md`.

---

**21. (b) Describe the HTTP request-response cycle with suitable examples.**

See answer for **Part B, Q.12(a)** in `fat01_2k24_anx.md`.

---

**22. (a) Illustrate the implementation of 2D and 3D transformations in CSS3 with code examples.**

See answer for **Part B, Q.11(b)** in `fat02_2k24_anx.md` for a similar question. A more focused example is below.

**2D Transformations** modify an element on a flat plane (X and Y axes).
**3D Transformations** add depth by introducing the Z-axis.

**HTML:**
```html
<div class="container">
    <div class="box two-d">2D</div>
    <div class="box three-d">3D</div>
</div>
```

**CSS:**
```css
.container {
    perspective: 800px; /* Creates a 3D space for child elements */
    padding: 100px;
}
.box {
    width: 150px;
    height: 150px;
    background: #007bff;
    color: white;
    display: inline-block;
    margin: 50px;
    transition: transform 0.5s ease;
}

/* 2D Transform Example */
.two-d:hover {
    transform: rotate(20deg) scale(1.2) translateX(30px);
}

/* 3D Transform Example */
.three-d:hover {
    transform: rotateY(180deg); /* Flips the element around the Y-axis */
}
```

---

**22. (b) Explain the features of HTML5 with examples of new input elements and tags.**

See answer for **Unit II, Topic 1 & 3** notes. Key features include:
-   **Semantic Tags:** `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`, `<aside>`. These give meaning to the page structure.
-   **Multimedia Tags:** `<audio>` and `<video>` for plugin-free media.
-   **Graphics:** `<canvas>` for 2D drawing and native support for SVG.
-   **New Input Elements and Attributes:** For richer forms.

**Examples of New Input Elements:**
```html
<form>
  <!-- Provides a native date picker -->
  <label>Date:</label>
  <input type="date" name="bday">

  <!-- Validates email format and shows a specialized mobile keyboard -->
  <label>Email:</label>
  <input type="email" name="email" required>

  <!-- Provides a slider control -->
  <label>Volume:</label>
  <input type="range" name="volume" min="0" max="100">

  <!-- Provides a color picker -->
  <label>Color:</label>
  <input type="color" name="favcolor">
</form>
```

---

**23. (a) Examine the core features and importance of DOM in web development.**

See answer for **Part B, Q.13(b)** in `fat02_2k25_anx.md`.

---

**23. (b) Explore the Object Oriented Techniques in JavaScript.**

See answer for **Unit III, Topic 11** notes. Key techniques include:
1.  **Encapsulation:** Bundling data (properties) and methods within objects.
2.  **Inheritance:** Achieved through the **prototype chain**. Objects inherit from other objects.
3.  **Constructor Functions (Pre-ES6):** Functions used with the `new` keyword to create multiple object instances. Methods are often added to the `prototype` for efficiency.
4.  **ES6 Classes:** Modern `class` syntax which is "syntactic sugar" over prototypal inheritance. It provides a cleaner way to define objects and handle inheritance using `class`, `constructor`, `extends`, and `super`.

---

**24. (a) Demonstrate the role of Human-Computer Interaction in designing user-friendly systems.**

See answer for **Part B, Q.11(b)** in `fat03_2k25_anx.md`.

---

**24. (b) Discuss the advantages and challenges of web scraping libraries for data extraction.**

**Advantages:**
-   **Automation:** Libraries automate the tedious manual process of data collection, saving immense time and effort.
-   **Speed and Scale:** They can extract data from thousands of pages far faster than any human.
-   **Abstraction:** High-level libraries like `requests` and `BeautifulSoup` simplify complex tasks like making HTTP requests and parsing messy HTML, making scraping accessible even to beginners.
-   **Power for Dynamic Sites:** Browser automation libraries like `Selenium` and `Puppeteer` can interact with JavaScript-heavy websites, enabling the extraction of dynamically loaded content.

**Challenges:**
-   **Brittleness:** Scrapers are tightly coupled to the target website's HTML structure. A small change in the website's layout can break the scraper completely.
-   **Anti-Scraping Measures:** Websites actively block scrapers using CAPTCHAs, IP bans, and dynamic class names, requiring scrapers to be more sophisticated (e.g., using proxies, rotating user agents).
-   **Handling Dynamic Content:** Scraping sites that use JavaScript requires slower, more resource-intensive browser automation tools.
-   **Legal and Ethical Risks:** Scraping can violate a site's Terms of Service, and scraping personal or copyrighted data can lead to legal action.

---

**25. (a) Analyse the process of handling GET and POST requests in a Node.js server application.**

See answer for **Unit V, Topic 5** notes.

---

**25. (b) Elaborate the CRUD operation performed on a NoSQL database.**

See answer for **Part B, Q.12(a)** in `fat03_2k25_anx.md`.

---

## PART- C (1 x 10 = 10 Marks)

**26. Design a web page for an E-commerce site using the Canvas API, including graphics and animations.**

This example creates a simple product display on a canvas and adds a pulsing "Sale" badge animation.

**HTML:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Canvas E-commerce Demo</title>
    <style>
        body { display: flex; justify-content: center; align-items: center; height: 100vh; background: #f0f0f0; }
        canvas { border: 1px solid #ccc; background: white; }
    </style>
</head>
<body>
    <canvas id="productCanvas" width="400" height="400"></canvas>
    <script>
        const canvas = document.getElementById('productCanvas');
        const ctx = canvas.getContext('2d');

        // --- Draw Static Graphics ---
        // Product Box
        ctx.fillStyle = '#e0e0e0';
        ctx.fillRect(100, 100, 200, 200);

        // Product Image Placeholder
        ctx.fillStyle = '#c0c0c0';
        ctx.fillRect(125, 125, 150, 100);
        ctx.fillStyle = 'white';
        ctx.font = '20px Arial';
        ctx.textAlign = 'center';
        ctx.fillText('Image', 200, 185);

        // Product Title
        ctx.fillStyle = 'black';
        ctx.font = 'bold 24px Arial';
        ctx.fillText('Cool Gadget', 200, 260);

        // Product Price
        ctx.fillStyle = '#28a745';
        ctx.font = '20px Arial';
        ctx.fillText('$99.99', 200, 290);

        // --- Animation ---
        let saleBadgeSize = 1.0;
        let growing = true;

        function animateSaleBadge() {
            // Clear only the area of the badge for redraw
            ctx.clearRect(260, 80, 80, 80);

            // Update size for pulsing effect
            if (growing) {
                saleBadgeSize += 0.01;
                if (saleBadgeSize >= 1.1) growing = false;
            } else {
                saleBadgeSize -= 0.01;
                if (saleBadgeSize <= 1.0) growing = true;
            }

            // Save context state
            ctx.save();
            
            // Apply scale transformation
            ctx.translate(300, 120); // Move origin to badge center
            ctx.scale(saleBadgeSize, saleBadgeSize);
            ctx.translate(-300, -120); // Move origin back

            // Draw Sale Badge
            ctx.fillStyle = 'red';
            ctx.beginPath();
            ctx.arc(300, 120, 30, 0, Math.PI * 2);
            ctx.fill();

            // Draw Sale Text
            ctx.fillStyle = 'white';
            ctx.font = 'bold 18px Arial';
            ctx.fillText('SALE!', 300, 125);

            // Restore context state
            ctx.restore();

            // Request the next frame
            requestAnimationFrame(animateSaleBadge);
        }

        // Start the animation
        animateSaleBadge();
    </script>
</body>
</html>
```