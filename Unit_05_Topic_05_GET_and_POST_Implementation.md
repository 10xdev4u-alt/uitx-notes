---
title: "Unit V: GET and POST Implementation in Node.js"
id: unit5-topic5-get-post
tags:
  - unit-5
  - nodejs
  - http
  - get-request
  - post-request
  - routing
aliases:
  - "Node.js GET and POST"
links:
  - "[[UITx/Unit_05_Topic_04_Event_Handling_in_NodeJS.md|Event Handling in Node.js]]"
  - "[[UITx/Unit_05_Topic_06_Connecting_to_NoSQL_Database.md|Connecting to NoSQL Database]]"
---

# Unit V, Topic 5: GET and POST Implementation in Node.js

> [!quote] A web server must do more than simply respond; it must interpret the user's intent. The HTTP methods `GET` and `POST` are the two most common verbs in this dialogue. `GET` requests data, while `POST` submits data. Handling these two methods correctly is a fundamental skill for building any interactive web application or API.

## 1. Handling Different HTTP Methods

In our basic HTTP server, we can inspect the `req.method` property of the request object to determine what kind of request the client is making. This allows us to create different logic for handling `GET`, `POST`, `PUT`, `DELETE`, etc.

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    if (req.method === 'GET') {
        // Handle GET request
    } else if (req.method === 'POST') {
        // Handle POST request
    } else {
        res.writeHead(405, { 'Content-Type': 'text/plain' }); // Method Not Allowed
        res.end('This server only supports GET and POST requests.');
    }
});
```

## 2. Implementing a `GET` Request Handler

Handling a `GET` request typically involves routing based on the URL and returning the appropriate resource. We have already seen a basic version of this.

Let's expand on it by parsing URL query parameters. The built-in `url` module can help with this.

### Example: `GET` with Query Parameters
This server will respond to a request like `http://localhost:3000/greet?name=Alice`.

```javascript
const http = require('http');
const url = require('url'); // Import the url module

const server = http.createServer((req, res) => {
    // Parse the request URL
    const parsedUrl = url.parse(req.url, true);
    const path = parsedUrl.pathname;
    const query = parsedUrl.query;

    if (req.method === 'GET' && path === '/greet') {
        const name = query.name || 'Guest'; // Default to 'Guest' if name is not provided
        
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end(`Hello, ${name}!`);
    } else {
        res.writeHead(404, { 'Content-Type': 'text/plain' });
        res.end('Not Found');
    }
});

server.listen(3000, () => {
    console.log('Server running on port 3000');
});
```
-   `url.parse(req.url, true)`: The `true` argument tells the module to parse the query string into an object.

## 3. Implementing a `POST` Request Handler

Handling a `POST` request is more complex because it involves receiving data in the request body. The body of a `POST` request arrives in **chunks** as a stream of data. We need to listen for these chunks and assemble them.

The `req` object is a readable stream that emits `data` and `end` events.

### Steps to Handle a `POST` Request:
1.  Check if `req.method` is `'POST'`.
2.  Create a variable (e.g., `body`) to accumulate the data chunks.
3.  Listen for the `'data'` event on the `req` object. Each time a chunk of data arrives, append it to your `body` variable.
4.  Listen for the `'end'` event on the `req` object. This event signifies that the entire body has been received.
5.  Inside the `'end'` event handler, you can now parse and process the complete `body`.

### Example: `POST` with JSON Data
This server will expect a `POST` request to `/users` with a JSON body like `{"name": "John"}`.

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    if (req.method === 'POST' && req.url === '/users') {
        let body = '';

        // 1. Listen for incoming data chunks
        req.on('data', (chunk) => {
            body += chunk.toString(); // Append chunk to body
        });

        // 2. Listen for the end of the request
        req.on('end', () => {
            try {
                const user = JSON.parse(body);
                console.log('Received user:', user);

                // Send a success response
                res.writeHead(201, { 'Content-Type': 'application/json' }); // 201 Created
                res.end(JSON.stringify({ message: `User ${user.name} created successfully.` }));
            } catch (error) {
                // Handle JSON parsing error
                res.writeHead(400, { 'Content-Type': 'text/plain' }); // 400 Bad Request
                res.end('Invalid JSON format.');
            }
        });

    } else {
        res.writeHead(404, { 'Content-Type': 'text/plain' });
        res.end('Not Found');
    }
});

server.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

### Testing the `POST` Request
You cannot test this with a browser's address bar. You need a tool like `curl` or Postman.

**Using `curl`:**
```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"John"}' http://localhost:3000/users
```
**Expected Response:**
```json
{"message":"User John created successfully."}
```

## 4. Exam-Oriented Insights

Handling `GET` and `POST` is the foundation of building APIs and web applications.

> [!question] **Potential 2-Mark Questions:**
> 1.  **How do you determine the HTTP method of an incoming request in a Node.js server?**
>     *Answer:* By inspecting the `req.method` property of the request object.
> 2.  **Why is handling a `POST` request more complex than a `GET` request in Node.js?**
>     *Answer:* Because the body of a `POST` request arrives as a stream of data chunks that must be collected and assembled before they can be processed.
> 3.  **Which two events are essential for processing the body of a `POST` request on the `req` object?**
>     *Answer:* The `'data'` event (to receive chunks) and the `'end'` event (to signal completion).
> 4.  **Which core Node.js module can be used to parse the query string from a URL?**
>     *Answer:* The `url` module.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a complete Node.js HTTP server that handles both a `GET` request with a query parameter and a `POST` request with a JSON body. Explain the asynchronous nature of receiving the `POST` request body and why it's handled with event listeners. Discuss the importance of setting appropriate status codes (e.g., `200`, `201`, `404`) and `Content-Type` headers in your responses.
