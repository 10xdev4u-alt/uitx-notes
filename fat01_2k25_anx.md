---
title: "FAT01 - 2025 - Answer Key"
id: fat01-2k25-anx
tags:
  - fat
  - answers
  - unit-1
  - unit-2
aliases:
  - "FAT01 2025 Answers"
links:
  - "[[UITx/fat01_2k25.md|FAT01 2025 Question Paper]]"
---

# CS22503 - User Interface Tools and Techniques
## FAT01 - 2025 - Answer Key

> [!note] This document provides detailed answers for the FAT01 (2025) question paper.

---

## PART A (10 x 2 = 20 Marks)

**1. Write the features of computer networks and Internet.**

**Computer Network Features:**
-   **Resource Sharing:** Allows sharing of hardware (printers), software, and files.
-   **Communication:** Facilitates communication via email, chat, and video conferencing.
-   **Reliability:** Data can be replicated on multiple computers, ensuring availability.
-   **Scalability:** Networks can be expanded to accommodate more users and devices.

**Internet Features:**
-   **Global Connectivity:** A worldwide network connecting millions of computers.
-   **Decentralized:** No single entity controls the internet, making it resilient.
-   **Packet Switching:** Data is broken into packets and sent independently, allowing for efficient and robust data transfer.

---

**2. Mention the characteristics of ARPANET.**

ARPANET (Advanced Research Projects Agency Network) was the precursor to the modern internet. Its key characteristics were:
1.  **Decentralization:** It was designed to be a decentralized network with no single point of failure, ensuring it could withstand potential attacks on any one node.
2.  **Packet Switching:** It was the first large-scale network to successfully implement packet switching, a revolutionary technique where data is broken into small packets for more efficient and resilient transmission.

---

**3. Write the importance of DNS.**

The Domain Name System (DNS) is crucial because it acts as the "phonebook of the Internet." Its primary importance is **translating human-readable domain names** (like `www.google.com`) into machine-readable **IP addresses** (like `142.250.196.196`). This allows users to access websites using easy-to-remember names instead of complex numerical IP addresses.

---

**4. Define the term reverse lookup with an example.**

**Reverse DNS lookup (rDNS)** is the process of querying the Domain Name System (DNS) to determine the domain name associated with a given IP address. This is the opposite of a forward DNS lookup, which finds the IP address for a domain name.

**Example:**
-   **Forward Lookup:** `google.com` -> `142.250.196.196`
-   **Reverse Lookup:** `142.250.196.196` -> `lhr25s34-in-f4.1e100.net` (one of Google's hostnames)
It is commonly used by mail servers to verify the legitimacy of incoming emails and help filter spam.

---

**5. Distinguish SMTP and PoP3.**

| Feature | SMTP (Simple Mail Transfer Protocol) | POP3 (Post Office Protocol 3) |
| :--- | :--- | :--- |
| **Primary Function** | **Sending** and transferring email between mail servers. | **Retrieving** email from a mail server to a client. |
| **Action** | It "pushes" mail from a client to a server, and from server to server. | It "pulls" mail from a server's mailbox for a user to read. |
| **Default Model** | Store-and-forward. | Download-and-delete (by default). |
| **Common Port** | Port 25 (server-to-server), Port 587 (client submission). | Port 110 (unencrypted), Port 995 (encrypted). |

---

**6. Why is DOM important? Give an example.**

The **Document Object Model (DOM)** is important because it provides a standard programming interface for web pages. It represents the HTML document as a logical tree of objects, allowing scripting languages like **JavaScript to dynamically access and manipulate the content, structure, and style of a web page** after it has loaded.

**Example:** Changing the text of a heading.
```html
<h1 id="greeting">Hello</h1>
<script>
    // JavaScript uses the DOM to find the h1 element and change its content.
    document.getElementById('greeting').textContent = 'Hello, World!';
</script>
```

---

**7. Sketch on HTML 5 and its goals.**

**HTML5** is the fifth and latest major version of HTML. It's a new standard designed to deliver rich content and interactive applications without needing external plugins like Flash.

**Sketch / Key Goals:**
-   **Native Multimedia:** Introduce `<audio>` and `<video>` tags for plugin-free media playback.
-   **Richer Semantics:** Add new semantic tags like `<header>`, `<nav>`, `<article>`, and `<footer>` to give more meaning to the page structure.
-   **Enhanced Forms:** Provide new input types (`date`, `email`, `color`) and attributes (`required`, `pattern`) for better user experience and validation.
-   **Advanced Graphics:** Integrate the `<canvas>` element for 2D drawing and SVG for vector graphics.
-   **Improved APIs:** Standardize APIs for features like Geolocation, Drag and Drop, and Web Storage (`localStorage`, `sessionStorage`).
-   **Backward Compatibility:** Ensure that old HTML4 websites continue to work in modern browsers.

---

**8. What are semantic and non-semantic tags?**

-   **Semantic Tags:** These are HTML tags that clearly describe their meaning and the type of content they hold to both the browser and the developer. They provide context.
    -   **Examples:** `<article>`, `<nav>`, `<footer>`, `<h1>`, `<table>`.

-   **Non-Semantic Tags:** These are tags that tell nothing about their content. They are used for grouping and styling purposes.
    -   **Examples:** `<div>` (a generic division) and `<span>` (for inline content).

---

**9. How do you caption the table using HTML tags? Give an example.**

You caption a table using the `<caption>` tag. It must be inserted immediately after the `<table>` tag. It provides a title or description for the table.

**Example:**
```html
<table>
  <caption>Monthly Sales Report</caption>
  <thead>
    <tr>
      <th>Month</th>
      <th>Sales</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>$50,000</td>
    </tr>
  </tbody>
</table>
```

---

**10. Mention the role of the data transfer object in the Drag and Drop feature. Write the syntax of the object to use in the program.**

The **`dataTransfer` object** plays a crucial role in the Drag and Drop API by holding the data that is being dragged during the operation. Its primary role is to store data when the drag starts and retrieve it when the drop occurs.

**Syntax:**
The `dataTransfer` object is a property of the event object passed to drag event handlers.
-   **To set data (in `dragstart` event):**
    ```javascript
    event.dataTransfer.setData('text/plain', 'This is the data to drag');
    ```
-   **To get data (in `drop` event):**
    ```javascript
    const data = event.dataTransfer.getData('text/plain');
    ```

---

## PART B (3 x 10 = 30 Marks)

**11. (a) Explain the computer network in detail. What are the topologies to connect the computers to share the information?**

A **computer network** is a collection of interconnected autonomous computers and other devices (like printers, servers) that are able to exchange data and share resources. The primary purpose of a network is to facilitate communication and resource sharing among its users.

**Key Components:**
-   **End Devices (Hosts):** The source or destination of data (e.g., PCs, smartphones).
-   **Intermediary Devices:** Devices that connect hosts and manage data flow (e.g., routers, switches).
-   **Network Media:** The channel through which data travels (e.g., cables, Wi-Fi).
-   **Protocols:** Rules governing data communication (e.g., TCP/IP).

**Network Topologies** refer to the physical or logical arrangement of a network.

1.  **Bus Topology:** All devices share a single communication line or cable.
    -   **Pros:** Simple, cheap.
    -   **Cons:** Entire network fails if the main cable fails.

2.  **Star Topology:** All devices are connected to a central hub or switch.
    -   **Pros:** Easy to manage, fault-tolerant (one node failure doesn't affect others).
    -   **Cons:** Central hub is a single point of failure.

3.  **Ring Topology:** Devices are connected in a circular loop. Data travels in one direction.
    -   **Pros:** Orderly data transfer.
    -   **Cons:** Failure of one node can break the ring.

4.  **Mesh Topology:** Every device is connected to every other device.
    -   **Pros:** Extremely robust and fault-tolerant.
    -   **Cons:** Very expensive and complex due to extensive cabling.

5.  **Tree Topology:** A hybrid of bus and star topologies. Groups of star-configured networks are connected to a linear bus backbone.
    -   **Pros:** Scalable and easy to manage in segments.
    -   **Cons:** Dependent on the main bus backbone.

---

**11. (b) What are internet protocols? Explain TCP and UDP in detail.**

**Internet protocols** are a set of rules that govern how data is formatted, transmitted, and received over the internet and other computer networks. They ensure that devices can communicate with each other in a standardized way. The most fundamental suite of protocols is TCP/IP.

At the Transport Layer, two of the most important protocols are TCP and UDP.

**TCP (Transmission Control Protocol)**
TCP is a **connection-oriented** protocol that provides **reliable, ordered, and error-checked** delivery of a stream of data between applications.

-   **Connection-Oriented:** It establishes a connection using a "three-way handshake" (`SYN`, `SYN-ACK`, `ACK`) before any data is sent. This ensures both ends are ready to communicate.
-   **Reliable Delivery:** TCP guarantees that every segment of data sent will reach its destination. It uses sequence numbers to track segments and requires acknowledgments (`ACKs`) from the receiver. If a segment is lost, TCP re-transmits it.
-   **Ordered Delivery:** TCP ensures that data is delivered to the application layer in the same order it was sent. It reassembles the segments in the correct sequence at the destination.
-   **Flow Control:** It manages the rate of data transmission to prevent the sender from overwhelming the receiver.
-   **Use Cases:** Web browsing (HTTP/HTTPS), email (SMTP), and file transfer (FTP), where data integrity and completeness are critical.

**UDP (User Datagram Protocol)**
UDP is a **connectionless** protocol that provides a simple but **unreliable** datagram service. It is often called a "fire-and-forget" protocol.

-   **Connectionless:** No handshake is performed. Data is simply sent to the destination without establishing a prior connection.
-   **Unreliable:** UDP does not guarantee that datagrams will arrive, nor does it guarantee they will arrive in order. There is no acknowledgment, re-transmission, or sequencing.
-   **Low Overhead:** Because it does not have the reliability mechanisms of TCP, UDP is very lightweight and fast.
-   **Use Cases:** Real-time applications where speed is more important than perfect reliability. This includes video streaming, online gaming, voice over IP (VoIP), and DNS lookups. Losing a single frame in a video stream is less disruptive than waiting for a re-transmission.

---

**12. (a) Explain the world wide web and its architecture with suitable diagrams.**

The **World Wide Web (WWW)**, or "the Web," is a global information system of interlinked documents and other web resources that are accessed via the Internet. It is a service that runs on top of the internet infrastructure.

**Distinction from the Internet:**
-   **The Internet:** The global physical network of computers, cables, and routers.
-   **The Web:** The system of documents and applications (like web pages) that uses the internet for transport.

**Foundational Technologies (by Tim Berners-Lee):**
1.  **HTML (HyperText Markup Language):** The language for structuring web pages.
2.  **URI (Uniform Resource Identifier):** A unique address for each resource on the web (e.g., a URL).
3.  **HTTP (HyperText Transfer Protocol):** The protocol for transferring web resources.

**WWW Architecture: The Client-Server Model**
The Web operates on a **client-server model**.

-   **Client:** A web browser (e.g., Chrome, Firefox) on a user's device. Its job is to request resources and render them.
-   **Server:** A web server (e.g., Apache, Nginx) that stores resources and responds to client requests.

**Diagram of Interaction:**
```
+-----------------+       +-----------------+       +-----------------+
|   Your Device   |       |   The Internet  |       |   Web Server    |
| (Web Browser)   |       | (Routers, DNS)  |       | (e.g., Apache)  |
+-----------------+       +-----------------+       +-----------------+
        |                         |                         |
1. User types URL                 |                         |
        |                         |                         |
        |----2. DNS Query-------->|                         |
        |<---3. IP Address-------|                         |
        |                         |                         |
        |----4. HTTP Request----->|------------------------>|
        |                         |                         |
        |<---5. HTTP Response-----|<------------------------|
        |                         |                         |
6. Render Page                    |                         |
        |                         |                         |
```

**Workflow:**
1.  A user enters a URL into the browser (client).
2.  The browser uses DNS to translate the domain name into an IP address.
3.  The browser establishes a TCP connection to the web server at that IP address.
4.  The browser sends an HTTP request to the server, asking for the specific resource.
5.  The server processes the request, finds the resource (e.g., an HTML file), and sends it back in an HTTP response.
6.  The browser receives the response, parses the HTML, and renders the web page, making subsequent requests for other resources like images, CSS, and JavaScript files as needed.

---

**12. (b) Discuss HTTP protocol and its request and response operations.**

See answer for **12. (a)** in `fat01_2k24_anx.md`. The content is identical.

---

**13. (a) Demonstrate the use of local storage and session storage with the help of different html programs.**

**Program 1: Local Storage (Persistent Data)**
`localStorage` is used to store data that persists even after the browser is closed. This is ideal for user preferences like a theme.

**`local_storage_demo.html`:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Local Storage Demo</title>
    <style id="theme-style"></style>
</head>
<body>
    <h1>Local Storage: Theme Preference</h1>
    <p>Your theme preference will be remembered even if you close the browser.</p>
    <button id="light-theme-btn">Light Theme</button>
    <button id="dark-theme-btn">Dark Theme</button>

    <script>
        const lightBtn = document.getElementById('light-theme-btn');
        const darkBtn = document.getElementById('dark-theme-btn');
        const styleTag = document.getElementById('theme-style');

        function applyTheme(theme) {
            if (theme === 'dark') {
                styleTag.innerHTML = 'body { background-color: #333; color: #fff; }';
            } else {
                styleTag.innerHTML = 'body { background-color: #fff; color: #000; }';
            }
        }

        lightBtn.addEventListener('click', () => {
            localStorage.setItem('theme', 'light');
            applyTheme('light');
        });

        darkBtn.addEventListener('click', () => {
            localStorage.setItem('theme', 'dark');
            applyTheme('dark');
        });

        // On page load, check for a saved theme
        const savedTheme = localStorage.getItem('theme');
        if (savedTheme) {
            applyTheme(savedTheme);
        }
    </script>
</body>
</html>
```

---

**Program 2: Session Storage (Temporary Data)**
`sessionStorage` is used for data that should only last for the duration of the browser tab session. This is ideal for temporary data, like information entered in a multi-step form.

**`session_storage_demo.html`:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Session Storage Demo</title>
</head>
<body>
    <h1>Session Storage: Form Data</h1>
    <p>Enter your name. It will be remembered if you refresh, but cleared if you close the tab.</p>
    
    <label for="username">Username:</label>
    <input type="text" id="username">
    <p id="greeting"></p>

    <script>
        const usernameInput = document.getElementById('username');
        const greeting = document.getElementById('greeting');

        // On input, save the value to sessionStorage
        usernameInput.addEventListener('input', (event) => {
            sessionStorage.setItem('tempUsername', event.target.value);
        });

        // On page load, check for a saved username for this session
        const savedUsername = sessionStorage.getItem('tempUsername');
        if (savedUsername) {
            usernameInput.value = savedUsername;
            greeting.textContent = `Welcome back to this session, ${savedUsername}!`;
        }
    </script>
</body>
</html>
```

---

**13. (b) Develop a web page to explain engineering admission. Use appropriate tags to explain the process in the form of well formatted text, audio and videos using HTML 5 tags.**

See answer for **13. (a)** in `fat01_2k24_anx.md`. The concept is identical, requiring the use of semantic tags like `<header>`, `<main>`, `<section>`, `<article>`, and media tags like `<audio>` and `<video>`. The following is a new example for this specific prompt.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Engineering Admission Process</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.7; color: #333; }
        header { background-color: #005a9c; color: white; padding: 20px; text-align: center; }
        main { max-width: 900px; margin: 20px auto; padding: 0 20px; }
        section { background-color: #fff; border: 1px solid #ddd; border-radius: 8px; padding: 20px; margin-bottom: 25px; }
        h2 { color: #005a9c; }
        video { max-width: 100%; border-radius: 8px; }
        audio { width: 100%; margin-top: 15px; }
    </style>
</head>
<body>

    <header>
        <h1>Guide to Engineering Admissions 2025</h1>
    </header>

    <main>
        <section>
            <h2>Step 1: Entrance Examination</h2>
            <p>The first crucial step is to appear for the national or state-level entrance examinations. Preparation is key to securing a high rank, which opens doors to top institutions.</p>
            <article>
                <h3>Common Entrance Exams:</h3>
                <ul>
                    <li>Joint Entrance Examination (JEE) - Main & Advanced</li>
                    <li>State Level Engineering Entrance Exams (e.g., TNEA, MHT-CET)</li>
                    <li>Private University Exams (e.g., BITSAT, VITEEE)</li>
                </ul>
            </article>
        </section>

        <section>
            <h2>Step 2: Counseling Process</h2>
            <p>After results are declared, qualified candidates must participate in the counseling process. This involves choice filling, document verification, and seat allotment based on rank and preference.</p>
            
            <h3>Listen to an Expert's Advice on Counseling</h3>
            <audio controls>
                <source src="counseling_advice.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
        </section>

        <section>
            <h2>Step 3: Admission and Campus Life</h2>
            <p>Once a seat is allotted, you complete the admission formalities at the respective college. This marks the beginning of your exciting journey into the world of engineering.</p>
            
            <h3>Watch a Glimpse of Campus Life</h3>
            <video controls poster="campus_poster.jpg">
                <source src="campus_tour.mp4" type="video/mp4">
                Your browser does not support the video element.
            </video>
        </section>
    </main>

    <footer>
        <p style="text-align:center; color: #777;">&copy; 2024 Admission Guides Inc.</p>
    </footer>

</body>
</html>
```