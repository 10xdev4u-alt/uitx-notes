---
title: "End Semester Exam - 2024 - Answer Key"
id: sem-2k24-anx
tags:
  - semester-exam
  - answers
  - unit-1
  - unit-2
  - unit-3
  - unit-4
  - unit-5
aliases:
  - "SEM 2024 Answers"
links:
  - "[[UITx/sem_2k24.md|SEM 2024 Question Paper]]"
---

# CS22503 – User Interface Tools and Techniques
## End Semester Examination - Answer Key (Dec 2024)

> [!note] This document provides detailed answers for the End Semester Examination (Dec 2024) question paper.

---

## PART- A (20 x 2 = 40 Marks)

**1. Distinguish between router and modem.**

| Feature | Modem (Modulator-Demodulator) | Router |
| :--- | :--- | :--- |
| **Primary Function** | It converts digital signals from a computer into analog signals for transmission over ISP lines (e.g., cable, DSL) and vice-versa. | It creates a local network and routes traffic between devices on that network and to the internet (via the modem). |
| **Connection** | Connects your home network to the Internet Service Provider (ISP). | Connects multiple devices (computers, phones) to each other and to the modem. |

In short, a modem brings the internet into your home, and a router distributes that internet connection to your devices.

---

**2. Outline the functionalities of web browsers.**

A web browser's primary functionalities are:
1.  **Requesting Resources:** Sending HTTP requests to web servers to fetch web content.
2.  **Interpreting & Rendering:** Parsing HTML, CSS, and executing JavaScript to display web pages visually to the user.
3.  **Navigation:** Allowing users to move between pages using hyperlinks, back/forward buttons, and bookmarks.
4.  **Caching:** Storing frequently accessed resources locally to speed up subsequent page loads.
5.  **Security:** Implementing security features like sandboxing, HTTPS enforcement, and phishing warnings to protect users.

---

**3. Sketch the salient characteristics of ARPANET.**

ARPANET was the precursor to the modern internet. Its salient characteristics were:
1.  **Decentralization:** It was designed as a distributed network with no central control point, making it resilient to the failure of any single node.
2.  **Packet Switching:** It pioneered the use of packet switching, where data is broken into small packets that travel independently and are reassembled at the destination. This was more efficient and robust than the circuit-switching model used by telephone networks.

---

**4. How do you find the IP address of a domain? Give an example.**

You can find the IP address of a domain using command-line tools like `nslookup` or `ping`.

**Using `nslookup`:**
This tool is specifically for DNS queries.
-   **Command:** `nslookup google.com`
-   **Example Output:**
    ```
    Server:  your.dns.server
    Address: 192.168.1.1

    Non-authoritative answer:
    Name:    google.com
    Addresses: 2404:6800:4007:82b::200e
             142.250.196.206
    ```

---

**5. Identify the suitable HTML tag to display the image in the web page. Give an example code.**

The suitable HTML tag is the `<img>` (image) tag. It is a self-closing tag.

**Example Code:**
```html
<img src="path/to/your/image.jpg" alt="A descriptive text for the image">
```
-   `src`: Specifies the path to the image file.
-   `alt`: Provides alternative text for screen readers and is displayed if the image cannot be loaded.

---

**6. Exemplify the 2D `matrix()` function. List its parameters.**

The `matrix()` function is a CSS `transform` function that combines all 2D transformations into one. It takes six parameters representing a transformation matrix.

**Syntax:** `transform: matrix(scaleX, skewY, skewX, scaleY, translateX, translateY);`

**Parameters:**
1.  `scaleX()`
2.  `skewY()`
3.  `skewX()`
4.  `scaleY()`
5.  `translateX()`
6.  `translateY()`

**Example:** `transform: matrix(1, -0.2, 0, 1, 0, 0);` would apply a skew of -0.2 along the Y-axis.

---

**7. Create a CANVAS of height 200, width 300, white background and 1px of border style using HTML.**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Canvas Example</title>
    <style>
        #myCanvas {
            background-color: white;
            border: 1px solid black; /* 1px border style */
        }
    </style>
</head>
<body>
    <canvas id="myCanvas" width="300" height="200"></canvas>
</body>
</html>
```

---

**8. Write the advantages of web storage over HTTP cookies.**

1.  **Larger Storage Capacity:** Web Storage (`localStorage` and `sessionStorage`) offers a much larger storage capacity (typically 5-10MB per domain) compared to cookies (around 4KB).
2.  **Reduced Network Traffic:** Web Storage data is not automatically sent with every HTTP request to the server, unlike cookies. This reduces network overhead and improves performance.
3.  **Simpler API:** The Web Storage API (`setItem`, `getItem`, `removeItem`) is simpler and more intuitive to use with JavaScript than parsing the `document.cookie` string.

---

**9. List the merits of client-side programming.**

1.  **Improved Responsiveness:** Client-side scripts (like JavaScript) can provide immediate feedback to users (e.g., form validation, UI updates) without waiting for a server response, making the application feel faster.
2.  **Reduced Server Load:** By handling tasks like validation and simple calculations on the client-side, it reduces the number of requests sent to the server, saving server resources.
3.  **Richer User Interfaces:** It enables the creation of complex, interactive user interfaces, including animations, drag-and-drop functionality, and dynamic content updates via AJAX.

---

**10. How do you create Arrays and Objects in JavaScript? Give an example.**

**Creating an Array:**
The most common way is using the array literal syntax `[]`.
-   **Example:** `const fruits = ["Apple", "Banana", "Cherry"];`

**Creating an Object:**
The most common way is using the object literal syntax `{}`.
-   **Example:**
    ```javascript
    const person = {
      firstName: "John",
      lastName: "Doe",
      age: 30
    };
    ```

---

**11. Is it possible to apply inheritance in JavaScript? Justify with an example.**

Yes, it is possible. JavaScript is a **prototype-based** object-oriented language, meaning objects can inherit properties and methods directly from other objects. ES6 introduced the `class` and `extends` keywords, which provide a cleaner syntax over this prototypal inheritance.

**Justification with Example (using ES6 classes):**
```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    return `${this.name} makes a noise.`;
  }
}

// Dog class inherits from Animal
class Dog extends Animal {
  speak() {
    return `${this.name} barks.`;
  }
}

const dog = new Dog('Buddy');
console.log(dog.speak()); // Output: Buddy barks.
```
Here, the `Dog` class inherits the `name` property and constructor from the `Animal` class.

---

**12. Write the syntax to convert JSON string into Object with example.**

The syntax is to use the built-in `JSON.parse()` method.

**Syntax:** `JSON.parse(jsonString)`

**Example:**
```javascript
const jsonString = '{"name":"John Doe","age":30,"isStudent":false}';

// Convert the JSON string into a JavaScript object
const userObject = JSON.parse(jsonString);

console.log(userObject.name); // Output: John Doe
console.log(userObject.age);  // Output: 30
```

---

**13. State the reason for web scraping.**

Web scraping is performed to **automatically extract large amounts of data from websites** and save it in a structured format for analysis or use in another application. Key reasons include:
-   **Market Research:** To monitor competitor prices and product catalogs.
-   **Data Collection:** To gather data for academic research or machine learning models.
-   **Lead Generation:** To collect contact information from public directories.
-   **Content Aggregation:** To create news feeds or job boards by pulling data from multiple sources.

---

**14. Present the python installation procedure in sequence to prepare for web scraping.**

1.  **Download Python:** Go to the official website `python.org` and download the latest stable Python 3 installer for your operating system.
2.  **Run Installer:** Run the installer. On Windows, ensure you check the box **"Add Python to PATH"**.
3.  **Verify Installation:** Open a terminal and run `python3 --version` to confirm it's installed.
4.  **Create Virtual Environment:** Navigate to your project folder and run `python3 -m venv venv` to create an isolated environment.
5.  **Activate Environment:** Run `source venv/bin/activate` (macOS/Linux) or `venv\Scripts\activate` (Windows).
6.  **Install Libraries:** Use `pip` to install the necessary scraping libraries: `pip install requests beautifulsoup4`.

---

**15. List out the goals of Human computer Interaction.**

The primary goals of HCI are to design computer systems that are:
1.  **Usable:** Easy to learn and efficient to use.
2.  **Useful:** They must accomplish the user's intended tasks and meet their needs.
3.  **Safe:** They should prevent users from making critical errors and provide ways to recover from mistakes.
4.  **Enjoyable:** They should provide a satisfying and pleasant user experience.

---

**16. What are the various human computer interaction styles?**

Interaction styles are the ways users communicate with a computer system. Major styles include:
1.  **Command Line Interface (CLI):** User types commands (e.g., `ls`, `cd`). Powerful for experts but hard for novices.
2.  **Menu-Driven Interface:** User selects options from a list of menus.
3.  **Form Fill-in:** User enters data into fields in a structured form.
4.  **Direct Manipulation:** User interacts directly with graphical objects on the screen (e.g., dragging and dropping a file).
5.  **Natural Language:** User communicates with the system using human language (e.g., voice assistants like Siri or Alexa).

---

**17. List the functionalities which can do with Node.JS.**

Node.js is a server-side JavaScript runtime environment used for:
-   Building fast and scalable **web servers and APIs** (REST, GraphQL).
-   Creating **real-time applications** like chat servers and online games using WebSockets.
-   Developing **streaming applications** for video or audio.
-   Building **command-line tools** and scripts.
-   Creating **microservices** as part of a larger distributed system.

---

**18. What applications demand the Node.JS role to process the data?**

Node.js is in high demand for applications that are **I/O-intensive** (involve a lot of input/output operations like network requests or database queries) and need to handle many concurrent connections. Examples include:
-   **Real-Time Chat Applications:** Require managing thousands of persistent connections.
-   **Data Streaming Services:** (e.g., Netflix) where data is sent in continuous streams.
-   **Single Page Application (SPA) Backends:** Serving data via APIs to front-end frameworks like React or Angular.
-   **API Gateways:** Handling a large volume of API requests and routing them to other microservices.

---

**19. Write the advantages of NOSQL.**

1.  **Flexible Schema:** NoSQL databases are often schema-less, allowing you to store documents with varying structures in the same collection. This makes it easy to evolve your application's data model.
2.  **Horizontal Scalability:** They are designed to scale out by distributing data across multiple servers, which is often cheaper and more effective than scaling up a single server.
3.  **High Performance:** They are optimized for specific data models and access patterns (e.g., key-value, document), often leading to better performance for large-scale applications compared to general-purpose relational databases.

---

**20. Distinguish between GET & POST METHOD.**

| Feature | GET | POST |
| :--- | :--- | :--- |
| **Purpose** | To **request** or retrieve data from a server. | To **submit** data to a server to create or update a resource. |
| **Data Location** | Data is appended to the URL as query parameters. | Data is sent in the **body** of the HTTP request. |
| **Visibility** | Data is visible in the URL, browser history, and server logs. | Data is not visible in the URL. |
| **Security** | Less secure for sensitive data. | More secure for sensitive data as it's not exposed in the URL. |
| **Idempotent** | Yes. Making the same GET request multiple times has the same effect. | No. Making the same POST request multiple times may create multiple resources. |

---

## PART- B (5 x 10 = 50 Marks)

**21. (a) Explain the various network topologies. Compare their designs.**

See answer for **Part B, Q.11(a)** in `fat01_2k24_anx.md`.

---

**21. (b) Discuss about the HTTP Request. Use its structure to clarify the request format of the client to contact the server.**

See answer for **Part B, Q.12(a)** in `fat01_2k24_anx.md`.

---

**22. (a) Develop the web page for the Indian tourism department. The web page must show the important tourist spots in India with the help of media tags to understand the user easily.**

See answer for **Part B, Q.13(b)** in `fat01_2k25_anx.md` for a similar example. The following is a new example for this specific prompt.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Incredible India Tourism</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; background: #eef; }
        header { background: linear-gradient(to right, #ff9933, #ffffff, #138808); color: #000080; text-align: center; padding: 2rem; }
        main { max-width: 1000px; margin: auto; padding: 20px; }
        .spot { background: white; margin-bottom: 30px; padding: 20px; border-radius: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1); }
        .spot h2 { border-bottom: 2px solid #ff9933; padding-bottom: 10px; }
        video, img { max-width: 100%; border-radius: 8px; }
        audio { width: 100%; margin-top: 15px; }
    </style>
</head>
<body>
    <header>
        <h1>Incredible India</h1>
        <p>Discover the wonders of Indian tourism.</p>
    </header>
    <main>
        <article class="spot">
            <h2>The Taj Mahal, Agra</h2>
            <p>An immense mausoleum of white marble, built between 1631 and 1648 by order of the Mughal emperor Shah Jahan in memory of his favourite wife, the Taj Mahal is the jewel of Muslim art in India and one of the universally admired masterpieces of the world's heritage.</p>
            <img src="taj_mahal.jpg" alt="The Taj Mahal">
            <h3>Listen to a short audio guide:</h3>
            <audio controls>
                <source src="taj_mahal_guide.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
        </article>
        <article class="spot">
            <h2>The Backwaters of Kerala</h2>
            <p>The Kerala backwaters are a network of interconnected canals, rivers, lakes and inlets, a labyrinthine system formed by more than 900 km of waterways. In the midst of this landscape, there are a number of towns and cities, which serve as the starting and ending points of backwater cruises.</p>
            <h3>Watch a video of a houseboat journey:</h3>
            <video controls poster="kerala_poster.jpg">
                <source src="kerala_backwaters.mp4" type="video/mp4">
                Your browser does not support the video element.
            </video>
        </article>
    </main>
</body>
</html>
```

---

**22. (b) What are selectors in CSS? Apply all selectors to illustrate its usage using a simple program.**

See answer for **Part B, Q.11(a)** in `fat02_2k25_anx.md`.

---

**23. (a) Write the Java Script program to demonstrate the Date object manipulation and function to display the welcome message to the user.**

This program will display the current date and time, and greet the user based on the time of day.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Date and Greeting Demo</title>
</head>
<body>
    <h1>Date Object and Greeting</h1>
    <div id="datetime-display"></div>
    <div id="greeting-message"></div>

    <script>
        function displayTimeAndGreet() {
            // 1. Create a new Date object
            const now = new Date();

            // 2. Manipulate the Date object to get components
            const dateString = now.toLocaleDateString();
            const timeString = now.toLocaleTimeString();
            const currentHour = now.getHours();

            // Display the current date and time
            document.getElementById('datetime-display').textContent = `Current Date: ${dateString}, Current Time: ${timeString}`;

            // 3. Function to display a welcome message
            let greeting;
            if (currentHour < 12) {
                greeting = "Good Morning!";
            } else if (currentHour < 18) {
                greeting = "Good Afternoon!";
            } else {
                greeting = "Good Evening!";
            }
            
            document.getElementById('greeting-message').textContent = greeting;
        }

        // Call the function when the page loads
        displayTimeAndGreet();
        
        // Optional: Update the time every second
        setInterval(displayTimeAndGreet, 1000);
    </script>
</body>
</html>
```

---

**23. (b) Create the bank web page signup form. Validate the user and his authentication to ensure that the valid account holder is signing in the portal.**

This example creates a signup form and uses JavaScript to validate that the passwords match and meet a minimum length requirement before allowing submission.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Bank Signup</title>
    <style>
        body { font-family: sans-serif; }
        form { max-width: 400px; margin: auto; padding: 20px; border: 1px solid #ccc; border-radius: 10px; }
        div { margin-bottom: 15px; }
        label { display: block; margin-bottom: 5px; }
        input { width: 100%; padding: 8px; box-sizing: border-box; }
        button { width: 100%; padding: 10px; background-color: #28a745; color: white; border: none; border-radius: 5px; }
        .error { color: red; font-size: 0.9em; }
    </style>
</head>
<body>
    <form id="signupForm">
        <h2>Create Your Bank Account</h2>
        <div>
            <label for="username">Username:</label>
            <input type="text" id="username" required>
        </div>
        <div>
            <label for="password">Password (min. 8 characters):</label>
            <input type="password" id="password" required minlength="8">
        </div>
        <div>
            <label for="confirmPassword">Confirm Password:</label>
            <input type="password" id="confirmPassword" required>
            <p id="passwordError" class="error"></p>
        </div>
        <button type="submit">Sign Up</button>
    </form>

    <script>
        const form = document.getElementById('signupForm');
        const password = document.getElementById('password');
        const confirmPassword = document.getElementById('confirmPassword');
        const passwordError = document.getElementById('passwordError');

        form.addEventListener('submit', function(event) {
            // Prevent the form from submitting by default
            event.preventDefault();

            // Clear previous error messages
            passwordError.textContent = '';

            // Validation logic
            let isValid = true;

            if (password.value.length < 8) {
                passwordError.textContent = 'Password must be at least 8 characters long.';
                isValid = false;
            }

            if (password.value !== confirmPassword.value) {
                passwordError.textContent = 'Passwords do not match.';
                isValid = false;
            }

            if (isValid) {
                alert('Signup successful! Redirecting to login...');
                // In a real application, you would send the data to the server here.
                // form.submit(); 
            }
        });
    </script>
</body>
</html>
```

---

**24. (a) Analyze the techniques used in web scraping. Discuss the challenges involved in web scraping.**

**Techniques in Web Scraping:**
1.  **HTML Parsing:** This is the most common technique. The scraper sends an HTTP request, receives the raw HTML, and then parses this HTML into a DOM tree. Libraries like Python's `BeautifulSoup` or JS's `Cheerio` are used to navigate this tree and extract data based on tags, classes, or IDs. This is effective for static websites.
2.  **Browser Automation (Headless Browsers):** For modern, dynamic websites (Single Page Applications) that load content using JavaScript, simple HTML parsing fails. Browser automation tools like `Selenium` (Python) or `Puppeteer` (JS) are used to control a real browser instance. The tool loads the page, executes the JavaScript, waits for content to render, and then extracts data from the final, fully-rendered DOM.
3.  **API Reverse Engineering:** Some scrapers monitor the network requests made by a web page to find the internal APIs it uses to fetch data. Calling these APIs directly is often faster and more reliable than parsing HTML, as the data is usually returned in a structured format like JSON.

**Challenges in Web Scraping:**
1.  **Dynamic Content:** Websites that heavily rely on JavaScript to load data cannot be scraped with simple HTTP request libraries.
2.  **Anti-Scraping Measures:** Websites actively try to block scrapers using techniques like:
    -   **CAPTCHAs:** Puzzles designed to distinguish humans from bots.
    -   **IP Rate Limiting/Blocking:** Blocking an IP address that makes too many requests too quickly.
    -   **Honeypot Traps:** Invisible links that, when followed by a scraper, lead to an IP ban.
3.  **Changing Website Structure:** Scrapers are brittle. If a website redesigns its layout and changes HTML tags or class names, the scraper will break and needs to be updated.
4.  **Legal and Ethical Issues:** Scraping can violate a website's Terms of Service, and scraping personal or copyrighted data can have serious legal consequences.

---

**24. (b) Assume the end user is not aware of computer knowledge. How do you design the system interface to understand and easy use of the system with the help of Human Computer Interface?**

See answer for **Part B, Q.7** in `fat02_2k24_anx.md` for a similar question. Designing for a non-technical user requires prioritizing simplicity, clarity, and confidence-building.

1.  **Simplicity and Minimalism:**
    -   **Action:** Remove all non-essential elements, options, and text. The interface should only present what is absolutely necessary for the task at hand.
    -   **Benefit:** Reduces cognitive load and prevents the user from feeling overwhelmed.

2.  **Clear and Obvious Affordances:**
    -   **Action:** Design elements to strongly suggest their function. Buttons should look clickable (e.g., with shadows and borders). Text that is not clickable should not be blue and underlined.
    -   **Benefit:** The user should be able to understand what is interactive just by looking at the screen, without prior knowledge.

3.  **Immediate and Constant Feedback:**
    -   **Action:** Every user action must have an immediate and obvious reaction. When a button is pressed, it should visually change. When a process is running, a loading indicator must be shown.
    -   **Benefit:** This reassures the user that the system is working and has registered their input, building confidence and preventing confusion.

4.  **Use of Familiar Metaphors:**
    -   **Action:** Use icons and concepts that relate to the real world. A trash can icon for deleting, a shopping cart for e-commerce, a folder for storing files.
    -   **Benefit:** Allows users to apply their real-world knowledge to the digital interface, making it more intuitive.

5.  **Forgiveness and Error Prevention:**
    -   **Action:** Design the system to prevent errors from happening (e.g., disable a "Submit" button until a form is complete). For destructive actions like deletion, use a confirmation dialog (e.g., "Are you sure you want to delete?").
    -   **Benefit:** This makes users feel safe to explore the system without fear of breaking something permanently.

---

**25. (a) Identify the steps involved to build the Node.JS server. Explain request response handling with a suitable program.**

See answer for **Part B, Q.12(b)** in `fat03_2k25_anx.md`.

---

**25. (b) What is CRUD operation? Write a Node.JS program to apply CRUD operations on the Employee database.**

See answer for **Part B, Q.12(a)** in `fat03_2k25_anx.md`. The example there uses a `Product` model, but the Mongoose methods and Express routing are identical for an `Employee` model.

---

## PART- C (1 x 10 = 10 Marks)

**26. Create an animation program to change the color of the box from blue to green with 2 second delay to assess the animation method effect in the real time applications.**

This program will create a box that starts an animation 2 seconds after the page loads. The animation will change its color from blue to green.

**HTML (`index.html`):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Delayed Animation</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Delayed Color Change Animation</h1>
    <div class="animated-box"></div>
    <p>The animation will start after a 2-second delay.</p>
</body>
</html>
```

**CSS (`style.css`):**
```css
/* 1. Define the keyframes for the color change */
@keyframes color-fade {
  from {
    background-color: blue;
  }
  to {
    background-color: green;
  }
}

.animated-box {
  width: 200px;
  height: 200px;
  background-color: blue; /* Initial color */
  
  /* 2. Apply the animation */
  animation-name: color-fade;
  animation-duration: 4s; /* How long the animation takes */
  animation-delay: 2s; /* The 2-second delay before it starts */
  animation-fill-mode: forwards; /* The box will stay green after the animation ends */
  animation-iteration-count: 1; /* Run the animation only once */
}
```

**Explanation:**
-   **`@keyframes color-fade`**: Defines an animation that transitions the `background-color` from `blue` to `green`.
-   **`animation-name`**: Applies our `color-fade` animation to the `.animated-box` element.
-   **`animation-duration: 4s`**: The color change will happen smoothly over 4 seconds.
-   **`animation-delay: 2s`**: This is the key property. It tells the browser to wait for 2 seconds after the element is rendered before starting the animation.
-   **`animation-fill-mode: forwards`**: This ensures that after the animation completes, the box remains at its final state (green color) instead of reverting to its initial state (blue color).
-   **Real-Time Application Assessment:** This effect is used in real-time applications to draw attention to an element after a certain period, guide a user's focus, or signal a state change that isn't immediate. For example, a "Still there?" popup could fade in after a period of inactivity.