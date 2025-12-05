---
title: "Unit V: Event Handling in Node.js"
id: unit5-topic4-event-handling
tags:
  - unit-5
  - nodejs
  - events
  - event-emitter
  - event-loop
alias:
  - "Node.js Events"
links:
  - "[[UITx/Unit_05_Topic_03_Creating_Web_Servers_with_HTTP.md|Creating Web Servers with HTTP]]"
  - "[[UITx/Unit_05_Topic_05_GET_and_POST_Implementation.md|GET and POST Implementation]]"
---

# Unit V, Topic 4: Event Handling in Node.js

> [!quote] The architecture of Node.js is built upon a foundation of events. From an incoming HTTP request to data being read from a file, many operations in Node.js are asynchronous and emit events to signal their completion. Understanding how to create, listen for, and handle these events is fundamental to mastering the Node.js runtime.

## 1. The Event-Driven Paradigm

As we discussed in the introduction to Node.js architecture, Node.js uses an **event-driven, non-blocking I/O model**. This means that instead of waiting for an operation to complete, Node.js registers a **callback function** that will be executed once the operation is finished and an event is emitted.

This pattern is central to everything in Node.js. The `http.createServer()` method we saw previously is a perfect example: the callback function `(req, res) => { ... }` is an event handler for the `'request'` event.

## 2. The `EventEmitter` Class

At the core of Node.js's event system is the **`events` module**, which provides the `EventEmitter` class. Many built-in Node.js objects, such as HTTP servers, streams, and child processes, inherit from `EventEmitter`.

The `EventEmitter` class allows us to create, emit, and listen for our own custom events.

### Key Methods of `EventEmitter`:
-   **`on(eventName, listener)`**: Adds a listener function for a specified event. You can have multiple listeners for the same event.
-   **`emit(eventName, [arg1], [arg2], ...)`**: Emits an event, causing all registered listeners for that event to be called in the order they were registered.
-   **`once(eventName, listener)`**: Adds a one-time listener function for an event. This listener is invoked only the next time the event is fired, after which it is removed.
-   **`removeListener(eventName, listener)`**: Removes a specified listener from an event.

### Creating a Custom Event Emitter
Let's create a simple example to demonstrate how `EventEmitter` works.

```javascript
// 1. Import the EventEmitter class from the 'events' module
const EventEmitter = require('events');

// 2. Create a new class that extends EventEmitter (optional but good practice)
class MyEmitter extends EventEmitter {}

// 3. Instantiate the emitter
const myEmitter = new MyEmitter();

// 4. Register a listener for the 'greet' event
myEmitter.on('greet', (name) => {
    console.log(`Hello, ${name}!`);
});

// Register another listener for the same event
myEmitter.on('greet', (name) => {
    console.log(`Greetings, ${name}. The event has occurred.`);
});

// Register a one-time listener
myEmitter.once('specialEvent', () => {
    console.log('This will only happen once.');
});

// 5. Emit the events
console.log("Emitting 'greet' event...");
myEmitter.emit('greet', 'Alice'); // Both 'greet' listeners will fire

console.log("\nEmitting 'specialEvent' event for the first time...");
myEmitter.emit('specialEvent'); // The 'once' listener will fire

console.log("\nEmitting 'specialEvent' event for the second time...");
myEmitter.emit('specialEvent'); // Nothing happens, the listener was removed
```

### Output:
```
Emitting 'greet' event...
Hello, Alice!
Greetings, Alice. The event has occurred.

Emitting 'specialEvent' event for the first time...
This will only happen once.

Emitting 'specialEvent' event for the second time...
```

## 3. Events in Practice: The HTTP Server

The `http.Server` object returned by `http.createServer()` is an `EventEmitter`. The callback function we pass to it is simply a convenience listener for the `'request'` event.

The following two server implementations are equivalent:

**Method 1: Passing a callback (shorthand)**
```javascript
const server = http.createServer((req, res) => {
    res.end('Hello, World!');
});
```

**Method 2: Using `.on()`**
```javascript
const server = http.createServer();

server.on('request', (req, res) => {
    res.end('Hello, World!');
});
```

The `server` object emits other events as well, such as `'connection'` when a new TCP stream is established, and `'close'` when the server closes.

## 4. Asynchronous Nature of Events

It's crucial to remember that events are handled asynchronously via the event loop. When you call `emit()`, the listeners are executed **synchronously** in the order they were registered. However, the event itself is often triggered by an asynchronous operation completing.

For example, in an HTTP server, the `'request'` event is only emitted after an asynchronous I/O operation (receiving a request over the network) has completed.

## 5. Exam-Oriented Insights

Understanding the event-driven nature of Node.js is fundamental.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the core module in Node.js for working with events?**
>     *Answer:* The `events` module, which provides the `EventEmitter` class.
> 2.  **What is the difference between `on()` and `once()` methods in `EventEmitter`?**
>     *Answer:* `on()` registers a listener that is called every time the event is emitted, while `once()` registers a listener that is called only the next time the event is emitted and is then removed.
> 3.  **Which method is used to trigger an event on an `EventEmitter` instance?**
>     *Answer:* The `emit()` method.
> 4.  **The `http.Server` object inherits from which class, making it event-driven?**
>     *Answer:* It inherits from the `EventEmitter` class.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a Node.js script that creates a custom `EventEmitter`, registers multiple listeners for an event (including a `once` listener), and then emits the event to trigger the listeners. Explain how the event-driven architecture of Node.js contributes to its non-blocking nature. Relate the concept of event listeners to the callback function used in `http.createServer()`.
