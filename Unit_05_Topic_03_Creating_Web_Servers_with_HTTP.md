---
title: "Unit V: Creating Web Servers with HTTP"
id: unit5-topic3-http-server
tags:
  - unit-5
  - nodejs
  - http
  - web-server
  - request
  - response
alias:
  - "Node.js HTTP Server"
links:
  - "[[UITx/Unit_05_Topic_02_Installation_and_Setup.md|Installation and Setup]]"
  - "[[UITx/Unit_05_Topic_04_Event_Handling_in_NodeJS.md|Event Handling in Node.js]]"
---

# Unit V, Topic 3: Creating Web Servers with HTTP

> [!quote] At the heart of any back-end application is the ability to listen for and respond to network requests. Node.js provides a powerful, built-in `http` module that allows us to create a web server from scratch, giving us fundamental control over the request and response cycle. Let us now learn to build the very foundation of a web application.

## 1. The `http` Module

The **`http` module** is a core module in Node.js that provides functionality for creating HTTP servers and clients. You do not need to install it with npm; it is part of the Node.js standard library.

To use it, you must first `require` it in your file:
```javascript
const http = require('http');
```

## 2. Creating a Simple HTTP Server

The primary method for creating a server is `http.createServer()`. This method takes a callback function as an argument. This callback function is executed each time a request is made to the server.

The callback function receives two arguments:
-   **`request` (or `req`):** An object containing information about the incoming HTTP request (e.g., URL, headers, method).
-   **`response` (or `res`):** An object used to send a response back to the client.

### The `listen()` Method
After creating the server, you must tell it to listen for incoming requests on a specific port and hostname. This is done with the `server.listen()` method.

### A Basic "Hello, World!" Server
Let's create a simple server that responds with "Hello, World!" to every request.

**`index.js`:**
```javascript
// 1. Import the http module
const http = require('http');

// 2. Define the hostname and port
const hostname = '127.0.0.1'; // localhost
const port = 3000;

// 3. Create the server
const server = http.createServer((req, res) => {
    // This callback runs for every request
    
    // Set the status code to 200 (OK)
    res.statusCode = 200;
    
    // Set the Content-Type header to indicate plain text
    res.setHeader('Content-Type', 'text/plain');
    
    // End the response, sending the content "Hello, World!"
    res.end('Hello, World!\n');
});

// 4. Start listening for requests
server.listen(port, hostname, () => {
    console.log(`Server running at http://${hostname}:${port}/`);
});
```

### Running the Server
1.  Save the code above as `index.js`.
2.  Open your terminal in the same directory.
3.  Run the command: `node index.js`
4.  Open your web browser and navigate to `http://127.0.0.1:3000` or `http://localhost:3000`. You will see the text "Hello, World!".

## 3. The Request (`req`) Object

The `request` object is an instance of `http.IncomingMessage`. It provides details about the client's request.

### Key Properties of `req`:
-   **`req.url`**: The URL string from the request. For a request to `http://localhost:3000/about?user=1`, `req.url` would be `/about?user=1`.
-   **`req.method`**: The HTTP method of the request (e.g., `'GET'`, `'POST'`)
-   **`req.headers`**: An object containing the request headers (e.g., `host`, `user-agent`).

## 4. The Response (`res`) Object

The `response` object is an instance of `http.ServerResponse`. It is used to build and send the response back to the client.

### Key Methods of `res`:
-   **`res.statusCode = code`**: Sets the HTTP status code for the response.
-   **`res.setHeader(name, value)`**: Sets a single header value.
-   **`res.writeHead(statusCode, [headers])`**: A convenient method to set the status code and headers in one call.
-   **`res.write(chunk)`**: Sends a chunk of the response body. This can be called multiple times.
-   **`res.end([data])`**: Signals that the response is complete. This method *must* be called on each response. You can optionally pass the final chunk of data here.

## 5. Handling Different Routes

You can use the `req.url` property to send different responses for different URLs (a basic form of routing).

```javascript
const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/html');

    if (req.url === '/') {
        res.end('<h1>Welcome to the Homepage</h1>');
    } else if (req.url === '/about') {
        res.end('<h1>About Us</h1>');
    } else {
        res.statusCode = 404; // Not Found
        res.end('<h1>404 - Page Not Found</h1>');
    }
});

server.listen(3000, '127.0.0.1', () => {
    console.log('Server running on port 3000');
});
```
In this example, visiting `http://localhost:3000/` shows the homepage, while `http://localhost:3000/about` shows the about page. Any other URL results in a 404 error.

> [!note] **Frameworks like Express**
> While it's essential to understand the `http` module, manually handling routing, request bodies, and other complexities becomes tedious. Frameworks like **Express.js** are built on top of the `http` module to simplify and abstract these tasks, making web server development much faster and more organized.

## 6. Exam-Oriented Insights

Creating a basic HTTP server is a fundamental Node.js skill.

> [!question] **Potential 2-Mark Questions:**
> 1.  **Which core Node.js module is used to create a web server?**
>     *Answer:* The `http` module.
> 2.  **What are the two arguments passed to the callback function of `http.createServer()`?**
>     *Answer:* The `request` object (representing the incoming request) and the `response` object (used to send a response back).
> 3.  **Which method must be called on the response object to signal that the response is complete?**
>     *Answer:* The `res.end()` method.
> 4.  **How can you determine the URL and HTTP method of an incoming request in a Node.js HTTP server?**
>     *Answer:* By accessing the `req.url` and `req.method` properties of the request object.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a complete Node.js script that creates a simple HTTP server. The server should handle at least two different routes (e.g., `/` and `/contact`) and return a `404 Not Found` error for any other route. Explain the roles of `res.statusCode`, `res.setHeader()`, and `res.end()` in constructing an HTTP response.
