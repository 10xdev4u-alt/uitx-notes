---
title: "Unit V Quiz: Introduction to Node.js"
id: unit5-quiz
tags:
  - unit-5
  - quiz
  - assessment
  - nodejs
  - http
  - crud
aliases:
  - "Unit 5 Assessment"
links:
  - "[[UITx/Unit_05_Topic_07_CRUD_Operations_with_NodeJS.md|CRUD Operations with Node.js]]"
---

# Unit V Quiz: Introduction to Node.js

> [!note] This quiz is designed to test your understanding of the server-side concepts covered in Unit V, including the Node.js runtime, its architecture, and its interaction with databases.

## Section 1: Quiz Questions (Multiple Choice / Short Answer)

1.  Node.js is a ______.
    a) Programming Language
    b) Web Browser
    c) JavaScript Runtime Environment
    d) Database
2.  What is the core architectural model of Node.js that allows it to handle many concurrent connections efficiently?
3.  Which built-in Node.js module is used to create a web server?
4.  What is the command to initialize a new Node.js project and create a `package.json` file?
5.  The `http.createServer()` method takes a callback function that is executed for every incoming ______.
6.  In an HTTP server callback `(req, res) => {}`, what does the `req` object represent?
7.  To handle the data from a `POST` request, you need to listen for the `'data'` and `'end'` events on which object?
8.  What does ODM stand for in the context of a library like Mongoose?
9.  Which Mongoose method is used to find all documents in a collection?
    a) `findOne({})`
    b) `findAll({})`
    c) `find({})`
    d) `get({})`
10. What does CRUD stand for?

## Section 2: Reasoning Questions

1.  Explain the difference between Node.js's single-threaded, non-blocking I/O model and a traditional multi-threaded server model. Why is the Node.js model often more scalable?
2.  What is the relationship between Node.js and the V8 engine?
3.  Describe the roles of `package.json`, `node_modules`, and `package-lock.json` in a Node.js project.
4.  Explain the purpose of the `EventEmitter` class in Node.js and provide a simple example of its use.
5.  Why is handling a `POST` request in Node.js more complex than handling a `GET` request? Describe the process of receiving the `POST` body.
6.  What are the advantages of using an ODM like Mongoose over the native MongoDB driver for a complex application?
7.  Explain how the four CRUD operations map to the four main HTTP methods (`GET`, `POST`, `PUT`/`PATCH`, `DELETE`).
8.  Write a simple but complete Node.js HTTP server that responds with "Welcome" for the root URL (`/`) and "404 Not Found" for any other URL.
9.  What is the purpose of the `{ new: true }` option when using Mongoose's `findByIdAndUpdate()` method?
10. Why is it a bad idea to use Node.js for heavy, CPU-intensive tasks?

## Section 3: Real-World Cases

1.  **Case: A Real-Time Chat Application**
    You are tasked with building a real-time chat application that needs to support thousands of simultaneous users. Why would Node.js be an excellent choice for the back-end of this application?
2.  **Case: Project Collaboration**
    A developer joins a team working on a large Node.js project. After cloning the repository from Git, they notice there is no `node_modules` folder. What single command should they run to get the project ready, and which files will that command use to install the correct dependencies?
3.  **Case: API Endpoint for User Creation**
    You are building a REST API. You need to create an endpoint at `/api/users` that accepts `POST` requests with JSON data to create a new user. Outline the steps your Node.js server would need to take to handle this request and save the user to a MongoDB database using Mongoose.
4.  **Case: A Simple Web Server**
    A developer writes a Node.js server but forgets to include the `res.end()` method inside the request handler. What will be the observable behavior when a user tries to access the server in their browser?
5.  **Case: Data Retrieval API**
    You need to create a `GET` endpoint `/api/products?category=electronics` that retrieves all products belonging to a specific category. Using Mongoose, what query would you pass to the `Product.find()` method to achieve this?
6.  **Case: Updating a User Profile**
    A user updates their profile name on a website. The front-end sends a `PUT` request to `/api/users/:id` with the new name. Which Mongoose method would be most appropriate for finding the user by their ID and updating their information in a single operation?
7.  **Case: Deleting a Blog Post**
    An admin clicks a "Delete" button on a blog post. This triggers a `DELETE` request to `/api/posts/:id`. Which Mongoose method would you use to find and remove the corresponding document from the database?
8.  **Case: Choosing a Database**
    A startup is building a social media application where the structure of user posts might change frequently as new features are added. Why would a NoSQL database like MongoDB be a better choice than a traditional SQL database for this scenario?
9.  **Case: Custom Server Events**
    You are building a complex application and want to create a custom logging system. You want to be able to emit a `log` event from anywhere in your application and have a central logger handle writing it to a file. How would you use the `EventEmitter` class to achieve this?
10. **Case: Server Startup Message**
    What is the purpose of the callback function in `server.listen(port, () => { ... })`?

## Section 4: Rapid Fire Questions

1.  What is the file that contains metadata about a Node.js project?
2.  What command installs a package using npm?
3.  What is the default entry point file for a Node.js project?
4.  Which core module provides the `EventEmitter` class?
5.  What does the `req.url` property contain?
6.  What does BSON stand for?
7.  Which Mongoose method finds a single document by its `_id`?
8.  Which HTTP method is typically used for the "Update" operation in CRUD?
9.  What is the recommended version of Node.js for production use?
10. What does the `res.end()` method do?

## Section 5: All Possible 2-Mark Remember Questions

*From Unit V, Topic 1: Introduction to Node.js and its Architecture*
1.  What is Node.js?
2.  What is the core architectural principle that makes Node.js highly scalable?
3.  What is the role of the V8 engine in Node.js?
4.  What is NPM?

*From Unit V, Topic 2: Node.js Installation and Setup*
5.  What is the difference between the LTS and Current versions of Node.js?
6.  What is the purpose of the `package.json` file?
7.  Which npm command is used to create the `package.json` file?
8.  What is the `node_modules` folder, and should it be committed to version control?

*From Unit V, Topic 3: Creating Web Servers with HTTP*
9.  Which core Node.js module is used to create a web server?
10. What are the two arguments passed to the callback function of `http.createServer()`?
11. Which method must be called on the response object to signal that the response is complete?
12. How can you determine the URL and HTTP method of an incoming request in a Node.js HTTP server?

*From Unit V, Topic 4: Event Handling in Node.js*
13. What is the core module in Node.js for working with events?
14. What is the difference between `on()` and `once()` methods in `EventEmitter`?
15. Which method is used to trigger an event on an `EventEmitter` instance?
16. The `http.Server` object inherits from which class, making it event-driven?

*From Unit V, Topic 5: GET and POST Implementation in Node.js*
17. How do you determine the HTTP method of an incoming request in a Node.js server?
18. Why is handling a `POST` request more complex than a `GET` request in Node.js?
19. Which two events are essential for processing the body of a `POST` request on the `req` object?
20. Which core Node.js module can be used to parse the query string from a URL?

*From Unit V, Topic 6: Connecting to a NoSQL Database with Node.js*
21. What is a NoSQL database?
22. Why is MongoDB a good fit for Node.js applications?
23. What is the purpose of the `mongodb` npm package?
24. What is Mongoose, and what is one advantage of using it?

*From Unit V, Topic 7: Implementation of CRUD Operations with Node.js*
25. What does the acronym CRUD stand for?
26. In Mongoose, which method is used to add a new document to the database?
27. How would you find all documents in a Mongoose collection named `Product`?
28. What is the purpose of the `{ new: true }` option in `findByIdAndUpdate()`?

## Answers

### Section 1: Quiz Questions - Answers
1.  **1. c) JavaScript Runtime Environment** - **Concept:** Node.js Definition. **Reason:** Node.js is not a language itself but an environment that allows JavaScript to be executed outside of a web browser, on a server.
2.  **2. Event-driven, non-blocking I/O model** - **Concept:** Node.js Architecture. **Reason:** This model allows Node.js to handle thousands of concurrent connections efficiently on a single thread without getting blocked by I/O operations.
3.  **3. `http`** - **Concept:** Node.js Core Modules. **Reason:** The `http` module provides the necessary functions, like `http.createServer()`, to build an HTTP server.
4.  **4. `npm init`** - **Concept:** Node.js Project Setup. **Reason:** This command starts an interactive process to create the `package.json` file, which defines the project and its dependencies.
5.  **5. request** - **Concept:** HTTP Server. **Reason:** The callback function is an event listener for the `'request'` event, which fires every time the server receives a new HTTP request.
6.  **6. The incoming HTTP request from the client.** - **Concept:** HTTP Request/Response Cycle. **Reason:** The `req` object contains all information about the client's request, including the URL, headers, and method.
7.  **7. The `req` (request) object.** - **Concept:** Handling POST Data. **Reason:** The request object is a readable stream that emits `'data'` events as chunks of the body arrive and an `'end'` event when the body has been fully received.
8.  **8. Object Data Modeling** - **Concept:** Mongoose. **Reason:** Mongoose is an ODM library that provides a schema-based layer on top of the native MongoDB driver to model application data.
9.  **9. c) `find({})`** - **Concept:** Mongoose Read Operations. **Reason:** The `find()` method is used for querying documents. Passing an empty object `{}` as the query returns all documents in the collection.
10. **10. Create, Read, Update, Delete** - **Concept:** CRUD Operations. **Reason:** These are the four fundamental operations for managing data in any persistent storage system.

### Section 2: Reasoning Questions - Answers
1.  **1. Explanation:** A traditional model creates a new thread for each request, which consumes memory and can be inefficient if the thread is just waiting (blocking) for I/O. Node.js uses a single thread with an event loop. It delegates I/O operations and moves on to other tasks, handling callbacks when the I/O is complete. **Concept:** Node.js Architecture. **Reason:** This non-blocking approach allows a single thread to handle thousands of concurrent connections with minimal memory overhead, making it highly scalable for I/O-intensive applications.
2.  **2. Explanation:** Node.js is built on top of the V8 engine. V8 is the open-source JavaScript engine created by Google for the Chrome browser. **Concept:** Node.js and V8. **Reason:** Node.js uses V8 to compile JavaScript code into fast, optimized machine code, which is why Node.js has such high performance. V8 provides the "engine," and Node.js provides the runtime environment and APIs for server-side operations.
3.  **3. Explanation:**
    -   **`package.json`**: The project's manifest file. It contains metadata (name, version) and lists all project dependencies.
    -   **`node_modules`**: The folder where the actual code for all dependencies is downloaded and stored.
    -   **`package-lock.json`**: Records the exact version of every installed dependency, ensuring that the project is reproducible with the exact same package versions on any machine.
    **Concept:** NPM Dependency Management. **Reason:** This system allows for clear dependency definition, reproducible builds, and easy sharing of projects without having to share the massive `node_modules` folder.
4.  **4. Explanation:** The `EventEmitter` class, from the `events` core module, is the foundation of Node.js's event-driven architecture. It allows objects to emit named events that cause listener functions to be called. **Concept:** Event Handling. **Reason:**
    ```javascript
    const EventEmitter = require('events');
    const myEmitter = new EventEmitter();
    myEmitter.on('myEvent', () => console.log('Event fired!'));
    myEmitter.emit('myEvent'); // "Event fired!" is logged
    ```
    This allows for creating decoupled and asynchronous systems.
5.  **5. Explanation:** A `GET` request's data is typically in the URL (query parameters), which is immediately available in `req.url`. A `POST` request's data is in the request body, which can be large and arrives as a stream of data chunks. **Concept:** GET vs. POST Handling. **Reason:** To handle it, you must listen for the `'data'` event on the request object to collect each chunk, and then wait for the `'end'` event to signal that all chunks have arrived, at which point you can assemble and parse the complete body.
6.  **6. Explanation:** Mongoose provides a higher level of abstraction. Its main advantages are: 1) **Schemas**, which enforce a structure on your data and provide validation, reducing data-related bugs. 2) **Convenience Methods**, which simplify complex queries and operations. 3) **Middleware**, which allows running code before or after certain database operations. **Concept:** Mongoose vs. Native Driver. **Reason:** While the native driver is faster for simple operations, Mongoose's features lead to more organized, maintainable, and robust code for larger applications.
7.  **7. Explanation:**
    -   **Create** -> `POST`: Used to send data to a server to create a new resource.
    -   **Read** -> `GET`: Used to retrieve a resource from a server.
    -   **Update** -> `PUT` / `PATCH`: Used to modify an existing resource. `PUT` typically replaces the entire resource, while `PATCH` applies a partial update.
    -   **Delete** -> `DELETE`: Used to remove a resource.
    **Concept:** CRUD and RESTful APIs. **Reason:** This mapping provides a standard, predictable convention for building RESTful APIs.
8.  **8. Explanation:**
    ```javascript
    const http = require('http');
    const server = http.createServer((req, res) => {
        if (req.url === '/') {
            res.writeHead(200, { 'Content-Type': 'text/plain' });
            res.end('Welcome');
        } else {
            res.writeHead(404, { 'Content-Type': 'text/plain' });
            res.end('404 Not Found');
        }
    });
    server.listen(3000, () => console.log('Server running...'));
    ```
    **Concept:** HTTP Server Routing. **Reason:** This code checks the `req.url` property. If it matches the root path, it sends a 200 OK status and a welcome message. For any other URL, it sends a 404 Not Found status and message.
9.  **9. Explanation:** By default, `findByIdAndUpdate()` returns the document as it was *before* the update was applied. **Concept:** Mongoose Update Operations. **Reason:** Setting the option `{ new: true }` configures the method to return the modified document *after* the update has been successfully applied, which is often more useful in application logic.
10. **10. Explanation:** Node.js's event loop runs on a single thread. A long-running, CPU-intensive task (like a complex calculation) will block this thread. **Concept:** Node.js Architecture Limitations. **Reason:** While the CPU-intensive task is running, the event loop is blocked and cannot handle any other incoming requests or I/O callbacks, effectively freezing the entire application until the task is complete.

### Section 3: Real-World Cases - Answers
1.  **1. Case: A Real-Time Chat Application**
    *   **Why Node.js is a good choice:** Node.js's event-driven, non-blocking I/O architecture is ideal for handling a large number of simultaneous, long-lived connections (e.g., WebSockets) with low latency, which is exactly what a chat application requires.
    **Concept:** Node.js Use Cases. **Reason:** Its ability to efficiently manage many I/O-bound connections without getting blocked makes it highly scalable for real-time applications.
2.  **2. Case: Project Collaboration**
    *   **Command:** `npm install` (or `npm i`).
    *   **Files Used:** NPM will read the `package.json` file to see which dependencies are required and the `package-lock.json` file to install the exact versions of those dependencies that were used by the rest of the team.
    **Concept:** NPM Dependency Management. **Reason:** This ensures a consistent and reproducible build environment for all developers on the project.
3.  **3. Case: API Endpoint for User Creation**
    *   **Steps:**
        1.  Set up a route handler for `POST` requests to `/api/users`.
        2.  Listen for the `'data'` and `'end'` events on the `req` object to collect the incoming JSON body.
        3.  In the `'end'` handler, use `JSON.parse()` to convert the body string into a JavaScript object.
        4.  Create a new Mongoose `User` model instance with the parsed data.
        5.  Call the `.save()` method on the new user instance.
        6.  Send a `201 Created` success response back to the client with the newly created user data.
    **Concept:** CRUD Implementation. **Reason:** This follows the standard pattern for handling a `POST` request, processing the body, and performing a "Create" operation in the database.
4.  **4. Case: A Simple Web Server**
    *   **Behavior:** The browser will appear to be continuously loading and will eventually time out.
    *   **Reason:** The `res.end()` method is what signals to the server that the response is complete and can be sent to the client. Without it, the connection remains open, and the browser waits indefinitely for a response that never finishes.
    **Concept:** HTTP Response Cycle. **Reason:** `res.end()` is a mandatory final step in handling an HTTP request in Node.js.
5.  **5. Case: Data Retrieval API**
    *   **Mongoose Query:** `Product.find({ category: 'electronics' })`.
    *   **Concept:** Mongoose Read Operations. **Reason:** The `find()` method takes a query object as its first argument. By passing `{ category: 'electronics' }`, you are telling Mongoose to find all documents in the `products` collection where the `category` field is equal to `'electronics'`.
6.  **6. Case: Updating a User Profile**
    *   **Mongoose Method:** `User.findByIdAndUpdate(id, { name: newName }, { new: true })`.
    *   **Concept:** Mongoose Update Operations. **Reason:** This method is the most efficient choice as it combines finding the document by its unique ID and applying the update in a single atomic database operation.
7.  **7. Case: Deleting a Blog Post**
    *   **Mongoose Method:** `Post.findByIdAndDelete(id)`.
    *   **Concept:** Mongoose Delete Operations. **Reason:** This method is the most direct way to find a document by its unique ID and remove it from the database.
8.  **8. Case: Choosing a Database**
    *   **Why NoSQL is a good choice:** NoSQL databases like MongoDB are schema-less (or have a flexible schema). This means you can have documents with different structures in the same collection. **Concept:** NoSQL vs. SQL. **Reason:** For a social media app where you might frequently add new features (e.g., polls, location tags, different media types), a flexible schema allows you to evolve your data model easily without performing complex and costly database migrations, which would be required in a rigid SQL database.
9.  **9. Case: Custom Server Events**
    *   **Solution:** You would create a single, global instance of `EventEmitter`. The logging module would register a listener using `logger.on('log', (message) => { ... })`. From anywhere else in the application, you could import this logger instance and call `logger.emit('log', 'Some message')` to trigger the central logging function.
    **Concept:** EventEmitter. **Reason:** This decouples the code that generates log messages from the code that handles writing them, creating a clean, modular, and centralized logging system.
10. **10. Case: Server Startup Message**
    *   **Purpose:** The callback function is executed once the server has successfully started and is actively listening for requests on the specified port and host.
    *   **Concept:** Asynchronous Callbacks. **Reason:** It is used to provide confirmation that the server is running correctly, typically by logging a message to the console like "Server running on port 3000".

### Section 4: Rapid Fire Questions - Answers
1.  **1. What is the file that contains metadata about a Node.js project?** `package.json`.
2.  **2. What command installs a package using npm?** `npm install <package-name>`.
3.  **3. What is the default entry point file for a Node.js project?** `index.js`.
4.  **4. Which core module provides the `EventEmitter` class?** The `events` module.
5.  **5. What does the `req.url` property contain?** The URL string from the request, including the path and query string.
6.  **6. What does BSON stand for?** Binary JSON.
7.  **7. Which Mongoose method finds a single document by its `_id`?** `findById()`.
8.  **8. Which HTTP method is typically used for the "Update" operation in CRUD?** `PUT` or `PATCH`.
9.  **9. What is the recommended version of Node.js for production use?** LTS (Long-Term Support).
10. **10. What does the `res.end()` method do?** It signals that the response is complete and sends the final data to the client.

### Section 5: All Possible 2-Mark Remember Questions - Answers
1.  **1. What is Node.js?** - **Concept:** Node.js Definition. **Reason:** Node.js is a back-end JavaScript runtime environment that allows developers to execute JavaScript code on the server. It is built on the V8 engine.
2.  **2. What is the core architectural principle that makes Node.js highly scalable?** - **Concept:** Node.js Architecture. **Reason:** Its event-driven, non-blocking I/O model, which allows it to handle many concurrent connections efficiently on a single thread.
3.  **3. What is the role of the V8 engine in Node.js?** - **Concept:** V8 Engine. **Reason:** The V8 engine is Google's high-performance JavaScript engine that compiles JavaScript code into native machine code, making Node.js execution very fast.
4.  **4. What is NPM?** - **Concept:** NPM. **Reason:** NPM (Node Package Manager) is the default package manager for Node.js and the world's largest software registry, providing a vast ecosystem of open-source libraries (packages).
5.  **5. What is the difference between the LTS and Current versions of Node.js?** - **Concept:** Node.js Versions. **Reason:** The LTS (Long-Term Support) version is stable and recommended for production, while the Current version has the latest features but may be less stable.
6.  **6. What is the purpose of the `package.json` file?** - **Concept:** Project Manifest. **Reason:** It is a manifest file that contains metadata about a Node.js project and is used to manage the project's dependencies and scripts.
7.  **7. Which npm command is used to create the `package.json` file?** - **Concept:** NPM Commands. **Reason:** `npm init`.
8.  **8. What is the `node_modules` folder, and should it be committed to version control?** - **Concept:** Dependency Management. **Reason:** The `node_modules` folder contains all the downloaded code for a project's dependencies. It should NOT be committed to version control because it can be regenerated by running `npm install`.
9.  **9. Which core Node.js module is used to create a web server?** - **Concept:** Core Modules. **Reason:** The `http` module.
10. **10. What are the two arguments passed to the callback function of `http.createServer()`?** - **Concept:** HTTP Server. **Reason:** The `request` object (representing the incoming request) and the `response` object (used to send a response back).
11. **11. Which method must be called on the response object to signal that the response is complete?** - **Concept:** HTTP Response. **Reason:** The `res.end()` method.
12. **12. How can you determine the URL and HTTP method of an incoming request in a Node.js HTTP server?** - **Concept:** HTTP Request. **Reason:** By accessing the `req.url` and `req.method` properties of the request object.
13. **13. What is the core module in Node.js for working with events?** - **Concept:** Core Modules. **Reason:** The `events` module, which provides the `EventEmitter` class.
14. **14. What is the difference between `on()` and `once()` methods in `EventEmitter`?** - **Concept:** EventEmitter API. **Reason:** `on()` registers a listener that is called every time the event is emitted, while `once()` registers a listener that is called only the next time the event is emitted and is then removed.
15. **15. Which method is used to trigger an event on an `EventEmitter` instance?** - **Concept:** EventEmitter API. **Reason:** The `emit()` method.
16. **16. The `http.Server` object inherits from which class, making it event-driven?** - **Concept:** Node.js Architecture. **Reason:** It inherits from the `EventEmitter` class.
17. **17. How do you determine the HTTP method of an incoming request in a Node.js server?** - **Concept:** HTTP Request. **Reason:** By inspecting the `req.method` property of the request object.
18. **18. Why is handling a `POST` request more complex than a `GET` request in Node.js?** - **Concept:** GET vs. POST. **Reason:** Because the body of a `POST` request arrives as a stream of data chunks that must be collected and assembled before they can be processed.
19. **19. Which two events are essential for processing the body of a `POST` request on the `req` object?** - **Concept:** POST Handling. **Reason:** The `'data'` event (to receive chunks) and the `'end'` event (to signal completion).
20. **20. Which core Node.js module can be used to parse the query string from a URL?** - **Concept:** Core Modules. **Reason:** The `url` module.
21. **21. What is a NoSQL database?** - **Concept:** NoSQL Definition. **Reason:** A NoSQL database is a database that provides a mechanism for storing and retrieving data that is modeled in means other than the tabular relations used in relational databases. MongoDB is a popular example.
22. **22. Why is MongoDB a good fit for Node.js applications?** - **Concept:** Node.js & MongoDB. **Reason:** MongoDB stores data in BSON (Binary JSON), a format very similar to the JSON used natively in JavaScript, which makes data manipulation between the application and the database seamless.
23. **23. What is the purpose of the `mongodb` npm package?** - **Concept:** Database Drivers. **Reason:** It is the official native driver for Node.js, providing the necessary tools (like the `MongoClient` object) to connect to and interact with a MongoDB database.
24. **24. What is Mongoose, and what is one advantage of using it?** - **Concept:** ODM. **Reason:** Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. One advantage is that it allows you to define a strict Schema for your data, providing structure and built-in validation.
25. **25. What does the acronym CRUD stand for?** - **Concept:** CRUD Definition. **Reason:** Create, Read, Update, Delete.
26. **26. In Mongoose, which method is used to add a new document to the database?** - **Concept:** Mongoose Create. **Reason:** The `.save()` method on a new model instance, or the static `Model.create()` method.
27. **27. How would you find all documents in a Mongoose collection named `Product`?** - **Concept:** Mongoose Read. **Reason:** By using the `find()` method with an empty query object: `Product.find({})`.
28. **28. What is the purpose of the `{ new: true }` option in `findByIdAndUpdate()`?** - **Concept:** Mongoose Update. **Reason:** It ensures that the method returns the document *after* the update has been applied, rather than the original document before the update.
