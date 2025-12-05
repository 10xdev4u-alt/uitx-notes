---
title: "FAT03 - 2025 - Answer Key"
id: fat03-2k25-anx
tags:
  - fat
  - answers
  - unit-4
  - unit-5
aliases:
  - "FAT03 2025 Answers"
links:
  - "[[UITx/fat03_2k25.md|FAT03 2025 Question Paper]]"
---

# CS22503 - User Interface Tools and Techniques
## FAT03 - 2025 - Answer Key

> [!note] This document provides detailed answers for the FAT03 (2025) question paper, covering Web Scraping, HCI, and Node.js.

---

## PART A (10 x 2 = 20 Marks)

**1. Classify the programming languages commonly used for web scraping.**

Programming languages for web scraping can be classified based on their ecosystem and primary use case:

1.  **Python:** The most popular choice, known for its simple syntax and extensive libraries like `Requests` (for HTTP requests), `BeautifulSoup` (for HTML parsing), and `Scrapy` (for large-scale scraping).
2.  **JavaScript (with Node.js):** Excellent for scraping modern, dynamic websites that rely on JavaScript to load content. It uses libraries like `Puppeteer` or `Playwright` to control a headless browser.
3.  **Other Languages:** Languages like Ruby (with Nokogiri) and PHP (with Goutte) are also used but are less common than Python and JavaScript.

---

**2. Compare web scraping with traditional data extraction methods.**

| Feature | Web Scraping | Traditional Data Extraction (e.g., APIs, DB Dumps) |
| :--- | :--- | :--- |
| **Data Source** | Unstructured or semi-structured HTML from websites designed for humans. | Structured data sources like databases or dedicated APIs. |
| **Reliability** | **Brittle.** Scripts can break easily if the website's HTML structure changes. | **Robust.** APIs have a stable contract, making data extraction reliable. |
| **Access** | No explicit permission is needed, but may be against Terms of Service. | Requires explicit permission, authentication keys, and adherence to API rate limits. |
| **Process** | Involves fetching HTML, parsing it, and extracting data from the DOM. | Involves making a structured request to an endpoint and receiving structured data (e.g., JSON). |

---

**3. State the importance of Human-Computer Interaction in web scraping.**

HCI principles are surprisingly important for web scraping because a scraper acts as a "robotic user."
1.  **Easier Scraping:** Websites with good HCI design (clear, consistent, semantic HTML structure) are much easier to scrape because the data is logically organized and easy to target with selectors.
2.  **Harder Scraping:** Websites with poor HCI or those that intentionally obfuscate their structure (to prevent scraping) are harder to scrape. A scraper developer must reverse-engineer the user's interaction flow.

---

**4. Illustrate how screen design can impact user experience in HCI.**

Good screen design directly leads to a better user experience (UX) by reducing cognitive load and making interactions feel effortless.
-   **Good Design:** A login screen with clear labels, large input fields, and a prominent, brightly colored "Login" button has good **visual hierarchy** and **affordance**. This makes the process fast and reduces user frustration.
-   **Bad Design:** A cluttered screen with small fonts, poor contrast, and confusingly placed buttons forces the user to think hard about how to perform a simple task, leading to a negative UX, even if the system is functional.

---

**5. Interpret the ethical considerations of web scraping and data privacy.**

Ethical web scraping requires balancing the goal of data collection with respect for the website owner and user privacy.
-   **Respect `robots.txt`:** Adhere to the website's stated rules for bots.
-   **Rate Limiting:** Do not overload the server with rapid requests; scrape at a human-like pace.
-   **Data Privacy:** Never scrape or store Personally Identifiable Information (PII) that is not intended for public consumption. Scraping data from behind a login is a major privacy violation.
-   **Transparency:** Identify your scraper with a clear User-Agent string.

---

**6. Summarize the main features of Node.js that make it suitable for server-side development.**

1.  **Asynchronous, Non-Blocking I/O:** Its event-driven architecture allows it to handle many concurrent connections efficiently on a single thread, making it highly scalable for I/O-intensive applications.
2.  **V8 Engine:** It uses Google's high-performance V8 engine to compile JavaScript into fast machine code.
3.  **NPM (Node Package Manager):** It has the world's largest ecosystem of open-source libraries, providing ready-made solutions for almost any problem.
4.  **Single Language Stack:** Allows developers to use JavaScript for both the front-end and back-end, simplifying development.

---

**7. Analyze how Node.js handles asynchronous requests and responses.**

Node.js handles asynchronous operations using a **single-threaded event loop**.
1.  When an asynchronous request (e.g., a database query or file read) is made, Node.js does not wait for it to complete.
2.  It delegates the operation to the underlying system (e.g., libuv's worker threads).
3.  It immediately moves on to execute the next line of code.
4.  A **callback function** is registered for the asynchronous operation.
5.  When the operation completes, an event is placed in the event queue. The event loop picks up this event and executes the corresponding callback function, thus completing the request/response cycle without blocking the main thread.

---

**8. Enlist the significance of the event-driven model in Node.js?**

The significance of the event-driven model is that it enables **high scalability and concurrency with low resource usage**.
-   It allows a single thread to handle thousands of simultaneous connections without getting blocked by I/O operations.
-   This makes Node.js extremely efficient for real-time, data-intensive applications like chat servers, streaming services, and APIs, where the server spends most of its time waiting for network or database responses.

---

**9. Write the concept of non-blocking I/O in Node.js.**

**Non-blocking I/O** is a programming model where a program does not wait for an I/O (Input/Output) operation to complete. Instead of halting execution, the program initiates the I/O request and then immediately continues with other tasks. When the I/O operation is finished, the system notifies the program (typically via a callback or event) so it can process the result. This is the core principle that prevents the single thread in Node.js from getting stuck while waiting for slow operations like database queries or file access.

---

**10. Give the functionality of `require()` in NodeJs?**

The `require()` function is a built-in Node.js function used to **import modules** into the current file. It follows the CommonJS module system.
-   **Functionality:** When you call `require('module-name')`, Node.js looks for the specified module (either a core module, a file in your project, or a package in `node_modules`), executes its code once, and returns the exported content (usually an object or a function) from that module. This allows you to organize code into reusable, separate files.

---

## PART B (3 x 10 = 30 Marks)

**11. (a) Explain the steps to scrape data from a website using Python.**

The process of scraping a static website with Python typically involves four main steps using the `requests` and `BeautifulSoup` libraries.

**Step 1: Make an HTTP Request**
-   **Purpose:** To fetch the raw HTML content of the target web page.
-   **Tool:** The `requests` library.
-   **Action:** Use `requests.get(URL)` to send a GET request to the website's URL. It's crucial to check the response status code (e.g., using `response.raise_for_status()`) to ensure the request was successful (status 200).

**Step 2: Parse the HTML**
-   **Purpose:** To convert the unstructured HTML string into a structured, navigable object tree.
-   **Tool:** The `BeautifulSoup` library.
-   **Action:** Create a `BeautifulSoup` object by passing the HTML content from the request and a parser (e.g., `'lxml'`) to its constructor: `soup = BeautifulSoup(response.text, 'lxml')`.

**Step 3: Find and Extract the Data**
-   **Purpose:** To locate and extract the specific pieces of information you need from the parsed HTML tree.
-   **Tool:** `BeautifulSoup`'s methods.
-   **Action:** Use methods like `find()` (to get the first matching element) and `find_all()` (to get all matching elements) with selectors like tag names, class names, or IDs. Once an element is found, use `.text` to get its content and `.strip()` to clean whitespace.

**Step 4: Store the Data**
-   **Purpose:** To save the extracted, structured data for future use.
-   **Tool:** Python's built-in `csv` module or `json` module.
-   **Action:** Loop through your extracted data and write it row by row into a CSV file or serialize it into a JSON file. This makes the data portable and easy to analyze.

---

**11. (b) Illustrate the principles of Human-Computer Interaction (HCI) and explain how they contribute to effective screen design.**

See answer for **Unit IV, Topic 7** notes. The core principles are:
1.  **Visual Hierarchy:** Guiding the user's eye to the most important elements first using size, color, and placement. This contributes to effective design by making screens scannable and reducing the time it takes for a user to find what they need.
2.  **Consistency:** Ensuring that similar elements look and behave in a predictable way. This reduces cognitive load, as users don't have to re-learn interactions in different parts of the application.
3.  **Feedback:** Providing immediate and clear information about the result of a user's action. This makes users feel in control and reduces uncertainty (e.g., a success message after form submission).
4.  **Affordance:** Designing elements to visually suggest their function (e.g., a button that looks pressable). This makes the interface intuitive and easy to learn.
5.  **Simplicity/Minimalism:** Removing unnecessary elements and clutter. This helps users focus on the primary task and makes the interface feel clean and efficient.

---

**12. (a) Apply the concept of CRUD operations in a Node.js application with examples.**

CRUD stands for Create, Read, Update, and Delete. Here are examples of implementing these operations in a Node.js/Express application using Mongoose for a `Product` model.

**Prerequisite: `Product` Model**
```javascript
const productSchema = new mongoose.Schema({
  name: String,
  price: Number,
  category: String
});
const Product = mongoose.model('Product', productSchema);
```

**1. CREATE (using `POST`):** Add a new product.
```javascript
// Route: POST /products
app.post('/products', async (req, res) => {
  try {
    const newProduct = await Product.create(req.body);
    res.status(201).json(newProduct);
  } catch (error) {
    res.status(400).json({ message: error.message });
  }
});
```

**2. READ (using `GET`):** Get all products or a single product.
```javascript
// Route: GET /products
app.get('/products', async (req, res) => {
  const products = await Product.find({});
  res.json(products);
});

// Route: GET /products/:id
app.get('/products/:id', async (req, res) => {
  const product = await Product.findById(req.params.id);
  res.json(product);
});
```

**3. UPDATE (using `PUT`):** Modify an existing product.
```javascript
// Route: PUT /products/:id
app.put('/products/:id', async (req, res) => {
  const updatedProduct = await Product.findByIdAndUpdate(
    req.params.id, 
    req.body, 
    { new: true } // Return the updated document
  );
  res.json(updatedProduct);
});
```

**4. DELETE (using `DELETE`):** Remove a product.
```javascript
// Route: DELETE /products/:id
app.delete('/products/:id', async (req, res) => {
  const deletedProduct = await Product.findByIdAndDelete(req.params.id);
  res.json({ message: 'Product deleted', product: deletedProduct });
});
```

---

**12. (b) Demonstrate the steps to create a basic web server using Node.js.**

See answer for **Unit V, Topic 3** notes. The steps are:
1.  **Import the `http` module:** `const http = require('http');`
2.  **Define Host and Port:** `const hostname = '127.0.0.1'; const port = 3000;`
3.  **Create the Server:** Use `http.createServer()` with a callback function that handles `request` and `response` objects.
4.  **Handle the Request:** Inside the callback, check `req.url` and `req.method` to implement basic routing.
5.  **Send the Response:** Use `res.writeHead()` to set the status code and headers, and `res.end()` to send the response body and close the connection.
6.  **Start Listening:** Call `server.listen()` to make the server start listening for requests on the specified port.

**Complete Code:**
```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  if (req.url === '/') {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Welcome to the Home Page!');
  } else if (req.url === '/about') {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('This is the About Page.');
  } else {
    res.writeHead(404, { 'Content-Type': 'text/plain' });
    res.end('404 Not Found');
  }
});

server.listen(3000, '127.0.0.1', () => {
  console.log('Server is running on http://127.0.0.1:3000');
});
```

---

**13. (a) Explain the architecture of Node.js and how it handles asynchronous requests.**

See answer for **Part A, Q.7** and **Unit V, Topic 1** notes.

Node.js architecture is built on two main components:
1.  **V8 Engine:** Google's high-performance JavaScript engine that compiles JS to machine code.
2.  **Libuv:** A C++ library that provides the asynchronous, non-blocking I/O capabilities. It manages the event loop and a worker thread pool for handling intensive I/O operations.

**How it handles asynchronous requests:**
Node.js uses a **single-threaded event loop**.
1.  The main thread receives a request.
2.  If the request requires a blocking I/O operation (like a database query), Node.js does not wait. It delegates the task to the Libuv worker thread pool.
3.  The main thread is now free to handle other incoming requests.
4.  When the I/O operation is complete, the worker thread places a **callback function** into the event queue.
5.  The event loop continuously checks this queue. When it finds the completed event's callback, it executes it on the main thread, sending the final response.

This architecture allows Node.js to handle thousands of concurrent connections with high throughput and minimal memory usage, making it extremely scalable for I/O-bound applications.

---

**13. (b) Implement an event handling mechanism in Node.js and illustrate its importance in server-side applications.**

See answer for **Unit V, Topic 4** notes.

**Implementation:**
We can implement a custom event handler using the `EventEmitter` class from the `events` core module. This is useful for creating decoupled, modular applications.

```javascript
const EventEmitter = require('events');

// Create a custom Logger class that extends EventEmitter
class Logger extends EventEmitter {
  log(level, message) {
    // Emit an event with the log data
    this.emit('logMessage', { level, message, timestamp: new Date() });
  }
}

// Create an instance of our logger
const logger = new Logger();

// Register a listener to handle the 'logMessage' event
logger.on('logMessage', (data) => {
  console.log(`[${data.timestamp.toISOString()}] [${data.level.toUpperCase()}]: ${data.message}`);
});

// --- Usage in a server-side application ---
function processRequest(user) {
  console.log(`Processing request for ${user}`);
  // Emit a log event instead of directly calling console.log
  logger.log('info', `User ${user} logged in.`);
  
  if (!user) {
    logger.log('error', 'Attempted process with no user.');
  }
}

processRequest('Alice');
processRequest(null);
```

**Importance in Server-Side Applications:**
1.  **Decoupling:** The part of the application that generates an event (e.g., `processRequest`) does not need to know how the event is handled. The `Logger` is completely separate. This makes the code more modular and easier to maintain.
2.  **Centralization:** You can have a single, centralized place to handle all events of a certain type. In this example, all logging is handled by one listener, which could be easily modified to write to a file or a database without changing any other part of the application.
3.  **Asynchronous Flow:** Events are the foundation of Node.js's asynchronous nature. They allow different parts of an application to communicate and react to the completion of long-running tasks (like database queries or file reads) without blocking the main thread.