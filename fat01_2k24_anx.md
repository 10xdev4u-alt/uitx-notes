---
title: "FAT01 - 2024 - Answer Key"
id: fat01-2k24-anx
tags:
  - fat
  - answers
  - unit-1
  - unit-2
aliases:
  - "FAT01 Answers"
links:
  - "[[UITx/fat01_2k24.md|FAT01 Question Paper]]"
---

# CS22503 - User Interface Tools and Techniques
## FAT01 - Answer Key

> [!note] This document provides detailed answers for the FAT01 (2024-2025) question paper. The answers are structured to be clear, comprehensive, and aligned with the concepts covered in our sessions.

---

## PART A (10 x 2 = 20 Marks)

**1. List out the components of the computer network.**

A computer network consists of four main components:
1.  **End Devices (Hosts):** Devices that are the source or destination of data, such as computers, smartphones, and servers.
2.  **Intermediary Devices:** Devices that connect end devices and manage data flow, such as routers and switches.
3.  **Network Media:** The physical or wireless channel through which data travels, like Ethernet cables, fiber-optic cables, or Wi-Fi.
4.  **Protocols:** The set of rules that govern how data is formatted, transmitted, and received (e.g., HTTP, TCP/IP).

---

**2. Write the types of computer network architecture.**

There are two primary types of computer network architecture:
1.  **Client-Server Architecture:** A centralized model where powerful servers provide resources and services to multiple clients (e.g., a web server delivering a webpage to a user's browser).
2.  **Peer-to-Peer (P2P) Architecture:** A decentralized model where all devices (peers) have equal capabilities and can both request and provide resources to each other without a central server (e.g., BitTorrent).

---

**3. State the role of IP addresses in the internet.**

The role of an IP (Internet Protocol) address is to provide a unique numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. Its primary functions are:
1.  **Host or Network Interface Identification:** It uniquely identifies a device on the network.
2.  **Location Addressing:** It specifies the location of the device in the network, thereby establishing a path for data to be sent and received.

---

**4. Find and Write Host, Domain and Top level domain from the following: `ftp apple net`.**

Assuming the input is a typo for `ftp.apple.net`:
-   **Host Name:** `ftp` (This is a subdomain that specifies a particular server, often for File Transfer Protocol).
-   **Domain Name:** `apple.net`
-   **Top-Level Domain (TLD):** `net`

---

**5. Interpret the following line. Write its purpose. `GET / HTTP/1.1`.**

This line is the **Request-Line** of an HTTP request.
-   **`GET`**: This is the HTTP method, indicating that the client wishes to **retrieve** data from the server.
-   **`/`**: This is the request URI, representing the root (homepage) of the website.
-   **`HTTP/1.1`**: This is the version of the HTTP protocol being used.

**Purpose:** Its purpose is to ask the web server to retrieve the main page (homepage) of the website using the HTTP version 1.1 protocol.

---

**6. Write the structure of HTML5 document.**

A basic HTML5 document has the following structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page Title</title>
</head>
<body>
    <!-- Page content goes here -->
</body>
</html>
```
-   `<!DOCTYPE html>`: Declares the document type to be HTML5.
-   `<html>`: The root element of the page.
-   `<head>`: Contains meta-information about the document (e.g., title, character set).
-   `<body>`: Contains the visible content of the web page.

---

**7. Sketch about HTML DOM.**

The HTML DOM (Document Object Model) represents an HTML document as a logical tree structure. Each part of the document—elements, attributes, and text—is a node in this tree.

**Sketch:**
```
       [Document]
           |
         [html]
         /    \
      [head]  [body]
      /    \      |
   [meta] [title] [h1]
            |      |
          "Title" "Heading Text"
```
This tree structure allows JavaScript to access, traverse, and manipulate the content and structure of the web page dynamically.

---

**8. Give a suitable tag to present contents in Newspaper with an example.**

The most suitable tag is `<article>`. The `<article>` element represents a self-contained, independently distributable piece of content, which is ideal for a newspaper article.

**Example:**
```html
<article>
  <h2>Historic Peace Treaty Signed</h2>
  <p>After weeks of negotiations, world leaders signed a historic peace treaty today...</p>
  <p>More details to follow.</p>
</article>
```

---

**9. What are the advantages of RIA in Web applications?**

RIA (Rich Internet Application) is a web application that has many of the characteristics of desktop applications. Key advantages include:
1.  **Richer User Experience:** RIAs provide a more interactive, responsive, and engaging user interface compared to traditional static web pages.
2.  **Increased Responsiveness:** Technologies like AJAX allow RIAs to update parts of a page without a full reload, making them feel faster and more like a desktop application.
3.  **Offline Capabilities:** Some RIAs can be designed to work offline and synchronize data when a connection becomes available.

---

**10. Mention the role of the ACTION attribute in the HTML form tag.**

The `action` attribute in an HTML `<form>` tag specifies the URL where the form data should be sent for processing when the form is submitted.

**Example:**
```html
<form action="/submit-data.php" method="post">
  <!-- Input fields go here -->
</form>
```
In this example, when the form is submitted, the data will be sent to the `/submit-data.php` script on the server.

---

## PART B (3 x 10 = 30 Marks)

**11. (a) Explain the network topology with suitable diagrams. Apply the appropriate topologies to College Lab and, Shopping Mall with neat diagram.**

**Network Topology** refers to the arrangement of the various elements (links, nodes, etc.) of a computer network. It is the topological structure of a network and may be depicted physically or logically.

**Types of Network Topologies:**

1.  **Bus Topology:** All devices are connected to a single central cable, called the bus or backbone.
    -   **Diagram:** `D---D---D---D` (D = Device)
    -   **Pros:** Inexpensive and easy to install.
    -   **Cons:** If the main cable fails, the entire network is down. Performance degrades as more devices are added.

2.  **Star Topology:** All devices are connected to a central hub or switch.
    -   **Diagram:** A central hub with lines radiating out to each device.
    -   **Pros:** Easy to manage, and failure of one device does not affect others.
    -   **Cons:** If the central hub fails, the entire network fails.

3.  **Ring Topology:** Each device is connected to exactly two other devices, forming a single continuous pathway for signals through each node - a ring.
    -   **Diagram:** Devices connected in a circular loop.
    -   **Pros:** Performs better than a bus topology under heavy load.
    -   **Cons:** Failure of one device can disrupt the entire network.

4.  **Mesh Topology:** Every device is connected to every other device in the network.
    -   **Diagram:** A web of interconnected devices.
    -   **Pros:** Highly fault-tolerant and robust.
    -   **Cons:** Expensive and complex to install and manage due to the large amount of cabling.

5.  **Tree Topology:** A hybrid topology that combines characteristics of bus and star topologies. It consists of groups of star-configured workstations connected to a linear bus backbone cable.
    -   **Diagram:** A main cable with branches, each branch being a star topology.
    -   **Pros:** Scalable and easy to manage in segments.
    -   **Cons:** Failure of the central bus cable can cripple the network.

**Application:**

1.  **College Lab:**
    -   **Appropriate Topology:** **Star Topology**.
    -   **Reasoning:** A college lab typically has 30-60 computers that need to be managed centrally. A star topology, with each computer connected to a central switch, is ideal. It is easy to add or remove computers, troubleshoot individual connections without affecting others, and manage network access from a central point.
    -   **Diagram:**
        ```
              +----------+
              |  Switch  |
              +----------+
              /  |  |  |  \
             /   |  |  |   \
           [PC] [PC]...[PC] [Printer]
        ```

2.  **Shopping Mall (for Public Wi-Fi):**
    -   **Appropriate Topology:** **Mesh Topology**.
    -   **Reasoning:** A shopping mall requires widespread, reliable Wi-Fi coverage over a large and complex area. A wireless mesh network is perfect for this. Multiple access points (nodes) are placed throughout the mall. They connect to each other to create a wide area of coverage. If one access point fails, data can be automatically rerouted through other nodes, ensuring a robust and self-healing network for shoppers.
    -   **Diagram:**
        ```
           [AP1] ---- [AP2] ---- [AP3]
             |  \      / | \      / |
             |   \    /  |  \    /  |
             |    \  /   |   \  /   |
           [AP4] ---- [AP5] ---- [AP6]
             |          |          |
           (Internet Gateway) ...
        ```

---

**11. (b) Explain : a) SMTP b) DNS.**

**a) SMTP (Simple Mail Transfer Protocol)**

SMTP is an application-layer protocol used for sending and transferring email messages across the internet. It operates on a "store-and-forward" model.

**Architecture and Workflow:**
1.  **Composition:** A user composes an email using a Mail User Agent (MUA), like Outlook or Gmail.
2.  **Submission:** The user's MUA sends the email to their own mail server's Mail Submission Agent (MSA) using SMTP.
3.  **Transfer:** The sender's mail server, acting as a Mail Transfer Agent (MTA), looks up the recipient's domain in the DNS to find their mail server. It then uses SMTP to transfer the email to the recipient's MTA.
4.  **Delivery:** The recipient's MTA receives the email and passes it to a Mail Delivery Agent (MDA), which places it in the recipient's mailbox on the server.
5.  **Retrieval:** The recipient later uses a different protocol, like POP3 or IMAP, to retrieve the email from their mailbox.

**Key SMTP Commands:**
-   `HELO`/`EHLO`: Initiates the connection.
-   `MAIL FROM`: Specifies the sender's address.
-   `RCPT TO`: Specifies the recipient's address.
-   `DATA`: Signals the start of the email content (headers and body).
-   `QUIT`: Terminates the connection.

**b) DNS (Domain Name System)**

DNS is the internet's phonebook. It is a hierarchical and decentralized naming system that translates human-readable domain names (like `www.google.com`) into machine-readable IP addresses (like `172.217.16.132`).

**Importance and Workflow:**
1.  **User Request:** A user types a domain name into their browser.
2.  **Resolver Query:** The user's computer asks a local DNS server (the "resolver," often provided by the ISP) for the IP address.
3.  **Root Server:** If the resolver doesn't know the IP, it asks one of the 13 root DNS servers. The root server doesn't know the IP but directs the resolver to the appropriate Top-Level Domain (TLD) server (e.g., the `.com` server).
4.  **TLD Server:** The resolver asks the TLD server. The TLD server doesn't know the IP but directs the resolver to the authoritative name server for that specific domain (e.g., Google's name servers).
5.  **Authoritative Name Server:** The resolver asks the authoritative name server, which knows the IP address and sends it back.
6.  **Caching:** The resolver caches this IP address for a certain amount of time (defined by the TTL - Time To Live) so it can answer future requests for the same domain instantly.
7.  **Browser Connection:** The resolver returns the IP address to the browser, which can then establish a connection to the web server.

This hierarchical system makes the internet scalable and resilient, as it distributes the responsibility for managing domain names across the globe.

---

**12. (a) Illustrate the HTTP Request- Response with examples and explain their message structure.**

The HyperText Transfer Protocol (HTTP) operates on a client-server, request-response model. The client (e.g., a web browser) sends a request message to a server, and the server replies with a response message.

**HTTP Request Message Structure:**

1.  **Request Line:** The first line, specifying the method, path, and HTTP version.
    -   `GET /index.html HTTP/1.1`
2.  **Request Headers:** Key-value pairs providing information about the request or the client.
    -   `Host: www.example.com`
    -   `User-Agent: Mozilla/5.0 ...`
    -   `Accept: text/html`
3.  **Blank Line:** A single empty line (CRLF) separates the headers from the body.
4.  **Request Body (Optional):** Contains data being sent to the server, used with methods like `POST`.

**Example HTTP GET Request:**
```
GET /search?q=books HTTP/1.1
Host: www.google.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)
Accept: text/html
Connection: keep-alive

```
*(No body for a GET request)*

---

**HTTP Response Message Structure:**

1.  **Status Line:** The first line, specifying the HTTP version, a status code, and a reason phrase.
    -   `HTTP/1.1 200 OK`
2.  **Response Headers:** Key-value pairs providing information about the response or the server.
    -   `Date: Mon, 23 May 2025 22:38:34 GMT`
    -   `Server: Apache/2.4.1 (Unix)`
    -   `Content-Type: text/html; charset=UTF-8`
    -   `Content-Length: 155`
3.  **Blank Line:** A single empty line separates the headers from the body.
4.  **Response Body (Optional):** Contains the resource requested by the client (e.g., HTML document, JSON data, image).

**Example HTTP Response:**
```
HTTP/1.1 200 OK
Date: Mon, 23 May 2025 22:38:34 GMT
Server: Apache
Content-Type: text/html; charset=UTF-8
Content-Length: 155

<!DOCTYPE html>
<html>
<head>
  <title>Example Page</title>
</head>
<body>
  <h1>Hello, World!</h1>
</body>
</html>
```

---

**12. (b) Explain the working model of Internet protocols with suitable examples.**

The working model of Internet protocols is best described by the **TCP/IP Model**, which is a conceptual framework that standardizes the functions of a telecommunication or computing system in terms of abstraction layers. It consists of four layers.

**1. Application Layer:**
-   **Purpose:** This is the layer where user-facing applications and network services operate. It defines the protocols that applications use to exchange data.
-   **Protocols:**
    -   **HTTP/HTTPS:** For web browsing.
    -   **SMTP, POP3, IMAP:** For email.
    -   **FTP:** For file transfer.
    -   **DNS:** For domain name resolution.
-   **Example:** When you use a web browser, it uses HTTP (an application layer protocol) to request a web page from a server.

**2. Transport Layer:**
-   **Purpose:** This layer is responsible for providing end-to-end communication services for applications. It handles data segmentation, flow control, and error checking.
-   **Protocols:**
    -   **TCP (Transmission Control Protocol):** A connection-oriented protocol that guarantees reliable, ordered delivery of data. It performs a "three-way handshake" to establish a connection. Used for web browsing, email, and file transfer where data integrity is crucial.
    -   **UDP (User Datagram Protocol):** A connectionless protocol that is faster but does not guarantee delivery or order. Used for real-time applications like video streaming or online gaming where speed is more important than perfect reliability.
-   **Example:** When your browser requests a web page via HTTP, the transport layer uses TCP to break the HTTP request into segments, number them, and ensure they all arrive correctly at the server.

**3. Internet Layer (or Network Layer):**
-   **Purpose:** This layer is responsible for logical addressing and routing. It moves packets from their source to their destination across different networks.
-   **Protocols:**
    -   **IP (Internet Protocol):** The primary protocol. It defines IP addresses to uniquely identify devices on the network and is responsible for routing packets to their destination.
-   **Example:** The Internet Layer takes the TCP segments, encapsulates them into IP packets, and adds source and destination IP addresses. Routers on the internet use these IP addresses to forward the packets toward their final destination.

**4. Link Layer (or Network Interface Layer):**
-   **Purpose:** This is the lowest layer, responsible for the physical transmission of data over the network media. It deals with physical addresses (MAC addresses) and the hardware specifications of the network.
-   **Protocols:** Ethernet, Wi-Fi, PPP.
-   **Example:** The Link Layer takes the IP packets and encapsulates them into frames. It adds the MAC address of the next hop (e.g., the local router) and converts the data into electrical signals, light pulses, or radio waves to be sent over the physical medium.

---

**13. (a) Build a HTML to create a blog to address the temples in Tamilnadu using appropriate tags to present the information neatly. Accommodate the audio and video of the temples to present the information.**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Temples of Tamil Nadu</title>
    <style>
        body { font-family: sans-serif; line-height: 1.6; margin: 0; padding: 0; background: #f4f4f4; }
        header, footer { background: #333; color: #fff; text-align: center; padding: 1rem 0; }
        main { max-width: 800px; margin: 20px auto; padding: 20px; background: #fff; }
        article { border-bottom: 1px solid #ddd; padding-bottom: 20px; margin-bottom: 20px; }
        nav ul { padding: 0; list-style: none; }
        nav ul li { display: inline; margin-right: 20px; }
        nav a { color: #fff; text-decoration: none; }
        figure { margin: 0; }
        figcaption { font-style: italic; text-align: center; color: #555; }
        video, audio { max-width: 100%; margin-top: 15px; }
    </style>
</head>
<body>

    <header>
        <h1>Exploring the Majestic Temples of Tamil Nadu</h1>
        <nav>
            <ul>
                <li><a href="#madurai">Madurai</a></li>
                <li><a href="#thanjavur">Thanjavur</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article id="madurai">
            <h2>Meenakshi Amman Temple, Madurai</h2>
            <p>The Meenakshi Temple is a historic Hindu temple located on the southern bank of the Vaigai River in the temple city of Madurai, Tamil Nadu, India. It is dedicated to the goddess Meenakshi, a form of Parvati, and her consort, Sundareshwarar, a form of Shiva.</p>
            
            <figure>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Meenakshi_Amman_Temple_Towers.jpg/1280px-Meenakshi_Amman_Temple_Towers.jpg" alt="Towers of Meenakshi Amman Temple" style="width:100%;">
                <figcaption>The towering gopurams of the Meenakshi Temple.</figcaption>
            </figure>

            <h3>Listen to the Temple Chants</h3>
            <audio controls>
                <source src="temple_chants.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
        </article>

        <article id="thanjavur">
            <h2>Brihadeeswarar Temple, Thanjavur</h2>
            <p>The Brihadeeswarar Temple, also called Rajarajesvaram or Peruvudaiyār Kōvil, is a Hindu temple dedicated to Shiva located in Thanjavur, Tamil Nadu. It is one of the largest South Indian temples and an exemplary example of a fully realized Dravidian architecture.</p>
            
            <h3>Watch a Tour of the Great Living Chola Temple</h3>
            <video controls poster="thanjavur_poster.jpg">
                <source src="thanjavur_tour.mp4" type="video/mp4">
                Your browser does not support the video element.
            </video>
        </article>
    </main>

    <footer>
        <p>&copy; 2024 Temple Tours. All rights reserved.</p>
    </footer>

</body>
</html>
```

---

**13. (b) Write a HTML program to illustrate the use of CANVAS to draw 2D images and to store the content "HELLO SVCE" in browser using web storage technique.**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Canvas and Web Storage Demo</title>
    <style>
        body { font-family: sans-serif; text-align: center; }
        canvas { border: 2px solid black; margin-top: 20px; }
        button { font-size: 16px; padding: 10px; margin: 10px; }
        #storage-display { margin-top: 20px; font-size: 18px; color: green; }
    </style>
</head>
<body>

    <h1>HTML5 Canvas and Web Storage</h1>

    <section>
        <h2>Part 1: Canvas 2D Drawing</h2>
        <canvas id="myCanvas" width="400" height="200"></canvas>
    </section>

    <hr>

    <section>
        <h2>Part 2: Web Storage</h2>
        <button id="saveButton">Store "HELLO SVCE" in Local Storage</button>
        <button id="loadButton">Load from Local Storage</button>
        <div id="storage-display"></div>
    </section>

    <script>
        // --- Part 1: Canvas Drawing ---
        const canvas = document.getElementById('myCanvas');
        if (canvas.getContext) {
            const ctx = canvas.getContext('2d');

            // Draw a filled rectangle
            ctx.fillStyle = 'lightblue';
            ctx.fillRect(20, 20, 150, 80);

            // Draw a stroked circle
            ctx.beginPath();
            ctx.arc(250, 60, 40, 0, 2 * Math.PI);
            ctx.strokeStyle = 'red';
            ctx.lineWidth = 3;
            ctx.stroke();

            // Draw text
            ctx.font = '30px Arial';
            ctx.fillStyle = 'darkblue';
            ctx.fillText('Canvas Demo', 80, 150);
        }

        // --- Part 2: Web Storage ---
        const saveBtn = document.getElementById('saveButton');
        const loadBtn = document.getElementById('loadButton');
        const display = document.getElementById('storage-display');
        const storageKey = 'myMessage';
        const messageToStore = 'HELLO SVCE';

        // Save to localStorage
        saveBtn.addEventListener('click', () => {
            localStorage.setItem(storageKey, messageToStore);
            display.textContent = `Message "${messageToStore}" has been stored!`;
            console.log(`Stored: ${localStorage.getItem(storageKey)}`);
        });

        // Load from localStorage
        loadBtn.addEventListener('click', () => {
            const storedMessage = localStorage.getItem(storageKey);
            if (storedMessage) {
                display.textContent = `Loaded Message: ${storedMessage}`;
            } else {
                display.textContent = 'No message found in local storage.';
            }
        });
    </script>

</body>
</html>
