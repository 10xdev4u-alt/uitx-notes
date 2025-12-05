---
title: "Unit I Quiz: Introduction to WWW"
id: unit1-quiz
tags:
  - unit-1
  - quiz
  - assessment
  - www-intro
aliases:
  - "Unit 1 Assessment"
links:
  - "[[UITx/Unit_01_Topic_11_Generation_of_Dynamic_Web_Pages.md|Generation of Dynamic Web Pages]]"
---

# Unit I Quiz: Introduction to WWW

> [!note] This quiz is designed to test your understanding of the foundational concepts of the World Wide Web and its underlying technologies covered in Unit I. Approach each question with a clear mind and reflect on the knowledge we have accumulated.

## Section 1: Quiz Questions

1.  What was the primary innovation of ARPANET that forms the basis of modern internet communication?
    a) Circuit Switching
    b) Packet Switching
    c) Optical Fiber Communication
    d) Wireless Connectivity
2.  Which organization is primarily responsible for technical standards related to the World Wide Web, such as HTML and CSS?
    a) IETF (Internet Engineering Task Force)
    b) IEEE (Institute of Electrical and Electronics Engineers)
    c) ICANN (Internet Corporation for Assigned Names and Numbers)
    d) W3C (World Wide Web Consortium)
3.  Identify the three foundational technologies created by Tim Berners-Lee for the World Wide Web.
4.  In the context of the WWW client-server model, what is the role of a "client"?
5.  Which protocol is primarily used for *sending* email messages between mail servers?
    a) POP3
    b) IMAP
    c) SMTP
    d) HTTP
6.  True or False: POP3 typically keeps a copy of downloaded emails on the mail server by default.
7.  What is the unique architecture of FTP that involves two separate connections?
8.  In modern web-based chat applications, which technology is often used for real-time, full-duplex communication over a single TCP connection?
    a) HTTP Polling
    b) SMTP
    c) WebSockets
    d) DNS
9.  What does it mean for HTTP to be "stateless"?
10. Which HTTP method is considered "safe" and "idempotent" for retrieving data from a server without modifying it?

## Section 2: Reasoning Questions

1.  Explain why packet switching was a revolutionary concept for network design compared to circuit switching, particularly in the context of network resilience and efficiency.
2.  Why are Internet Standards crucial for the global functionality and continued growth of the internet? Provide at least two reasons.
3.  Why is it inaccurate to use the terms "Internet" and "World Wide Web" interchangeably?
4.  Describe how the client-server model facilitates the delivery of web pages from a server to a user's browser, outlining the main steps.
5.  An email client is configured to use POP3. Discuss the implications for accessing emails from multiple devices.
6.  A web developer is using standard FTP to upload sensitive company documents. What are the security risks, and what alternatives should be considered?
7.  Explain how HTTP/2's multiplexing feature addresses the "head-of-line blocking" issue prevalent in HTTP/1.1 and improves web performance.
8.  Why is the `POST` HTTP method generally considered neither safe nor idempotent, unlike `GET` or `PUT`?
9.  Consider a scenario where a user submits a form on a website that registers a new account. Briefly describe the role of server-side scripting in processing this action and generating a personalized success message.
10. How does the use of client-side scripting (e.g., JavaScript with AJAX) make a dynamic web page appear more responsive and interactive without requiring full page reloads?

## Section 3: Real-World Cases

1.  **Case: E-commerce Checkout**
    A user completes a purchase on an e-commerce website. As they click "Place Order," what HTTP method is most likely used to send their order details to the server, and why?
2.  **Case: Video Streaming Site**
    When you open a video streaming website, the initial page loads quickly, but then the video content starts buffering. What might be happening at the network level (consider HTTP and general data transfer) that causes this initial quick load followed by a delay for the video?
3.  **Case: Company-Internal Wiki**
    A small company uses an internal wiki for documentation. Initially, it was just static HTML files. Now, they want to allow employees to edit pages directly through a web interface. What type of web page generation (static/dynamic) would be required, and what technologies (client-side/server-side/database) would be involved?
4.  **Case: Email Synchronization**
    You access your email from your laptop, your smartphone, and a webmail interface, and you want all devices to show the same read/unread status and folder structure. Which email retrieval protocol (POP3 or IMAP) would be most suitable for this scenario, and why?
5.  **Case: Online Gaming Chat**
    In an online multiplayer game, players need to send and receive messages from each other instantly. What kind of communication model (client-server vs. P2P) and underlying technology (e.g., WebSockets) would be most efficient for this real-time messaging, and why?
6.  **Case: Broken Image Link**
    You visit a website, and one of the images doesn't load, showing a broken icon instead. When you inspect the network traffic, what HTTP status code would you most likely see associated with the request for that image, and what does it indicate?
7.  **Case: Website Migration**
    A popular blog moves its content from an old domain (`oldblog.com`) to a new domain (`newblog.com`). To ensure that old bookmarks and search engine links still work, what HTTP status code should be used when a request comes to `oldblog.com` for content now hosted on `newblog.com`, and why?
8.  **Case: Large File Upload**
    A user needs to upload a very large video file to a cloud storage service. Which file transfer protocol (FTP, SFTP, HTTP with specific methods) would be most appropriate, considering efficiency for large files and security? Justify your choice.
9.  **Case: Social Media Feed Update**
    You are scrolling through a social media feed, and new posts appear automatically without you refreshing the entire page. Describe how AJAX likely plays a role in this seamless feed update.
10. **Case: International Website Access**
    A website is accessed by users globally. When a user in Japan accesses the site, the browser sends an `Accept-Language` header. How does this header contribute to delivering a better user experience, and what part of the HTTP request is it?

## Section 4: Rapid Fire Questions

1.  What does `RFC` stand for?
2.  Who invented the World Wide Web?
3.  Is HTTP/1.1 a stateful or stateless protocol?
4.  Which HTTP method is generally used for creating new resources on a server?
5.  What is the default unencrypted port for SMTP?
6.  Which FTP mode helps overcome client-side firewall issues?
7.  What is the purpose of a URI?
8.  Name a server-side scripting language mentioned in Unit I.
9.  What port does HTTPS typically use?
10. What was the name of the precursor to the internet developed in the 1960s?

## Section 5: All Possible 2-Mark Remember Questions

*From Unit I, Topic 1: Introduction to Computer Networks*
1.  What is a computer network?
2.  Differentiate between packet switching and circuit switching.
3.  What was the significance of ARPANET?
4.  List two examples of end devices and two examples of intermediary devices.

*From Unit I, Topic 2: Internet Standards*
5.  What is the purpose of an Internet Standard?
6.  Name two major internet standards organizations and their primary focus.
7.  What is an RFC?
8.  Why is interoperability important?

*From Unit I, Topic 3: Introduction to WWW*
9.  Distinguish between the Internet and the World Wide Web.
10. Who invented the World Wide Web?
11. List the three foundational technologies of the Web.
12. What is a URL?

*From Unit I, Topic 4: WWW Architecture*
13. Explain the client-server model in the context of the WWW.
14. What is the primary role of a web browser?
15. List two key functions of a web server.
16. How do HTTP, HTML, and URI collectively enable the WWW architecture?

*From Unit I, Topic 5: Simple Mail Transfer Protocol (SMTP)*
17. What is the primary function of SMTP?
18. Name the four main components of an email system.
19. Which port is commonly used for client mail submission with encryption?
20. What does the `DATA` command signify in an SMTP session?

*From Unit I, Topic 6: Post Office Protocol 3 (POP3)*
21. What is the primary function of POP3?
22. Describe the "download-and-delete" model of POP3.
23. Which port is used for secure POP3 connections?
24. State one key difference between POP3 and IMAP.

*From Unit I, Topic 7: File Transfer Protocol (FTP)*
25. What is the primary purpose of FTP?
26. Explain the two types of connections used by FTP.
27. Differentiate between active and passive FTP modes.
28. Why is standard FTP considered insecure?

*From Unit I, Topic 8: Chat*
29. What is the primary characteristic that distinguishes chat from email?
30. Name an early chat protocol and one of its key features.
31. What is the main advantage of using WebSockets for modern web-based chat?
32. Briefly explain a privacy concern associated with client-server chat models.

*From Unit I, Topic 9: Overview of HTTP*
33. What does "stateless" mean in the context of HTTP?
34. Name two key improvements introduced in HTTP/1.1 over HTTP/1.0.
35. What is the main advantage of HTTP/2's multiplexing feature?
36. Briefly explain the difference between HTTP and HTTPS.

*From Unit I, Topic 10: HTTP Request – Response*
37. List the three main parts of an HTTP request.
38. What is the purpose of the `GET` HTTP method?
39. What does an HTTP status code of `200 OK` signify?
40. Give an example of a `4xx` status code and its meaning.

*From Unit I, Topic 11: Generation of Dynamic Web Pages*
41. What is the primary difference between a static and a dynamic web page?
42. Name two popular server-side scripting languages/frameworks used for dynamic web page generation.
43. What is the role of a database in generating dynamic web pages?
44. How does AJAX enhance the user experience of dynamic web pages?

## Answers

### Section 1: Quiz Questions - Answers
1.  **1. b) Packet Switching** - **Concept:** Computer Network Fundamentals. **Reason:** Packet switching allows data to be broken into independent packets, enabling decentralized and fault-tolerant communication, which was ARPANET's key innovation for resilience against disruptions.
2.  **2. d) W3C (World Wide Web Consortium)** - **Concept:** Internet Standards Organizations. **Reason:** The W3C develops standards specifically for the World Wide Web, including HTML, CSS, and XML, defining how web content is structured and presented. The IETF focuses on core internet protocols.
3.  **3. HTML, URI, HTTP** - **Concept:** Foundational Web Technologies. **Reason:** Tim Berners-Lee developed HTML for structuring web documents, URI for identifying resources, and HTTP for transferring those documents across the network, forming the core infrastructure of the Web.
4.  **4. A client (web browser) initiates requests for web resources from a server.** - **Concept:** WWW Architecture (Client-Server Model). **Reason:** In the client-server model, the client acts as the service requester, actively seeking out and requesting data or services from the server.
5.  **5. c) SMTP** - **Concept:** Email Protocols. **Reason:** SMTP (Simple Mail Transfer Protocol) is specifically designed and used for sending outgoing email messages and transferring them between mail servers. POP3 and IMAP are for retrieval.
6.  **6. False** - **Concept:** POP3 Functionality. **Reason:** POP3, by default, is a "download-and-delete" protocol. When emails are retrieved using POP3, they are typically removed from the server, making it difficult to access them from other devices. (Though some clients offer an option to "leave a copy on the server," this is not the default behavior of the protocol itself.)
7.  **7. Separate Control Connection and Data Connection** - **Concept:** FTP Architecture. **Reason:** FTP uniquely uses two distinct TCP connections: one for sending commands and receiving responses (control connection) and another for the actual transfer of file data and directory listings (data connection).
8.  **8. c) WebSockets** - **Concept:** Modern Chat Technologies. **Reason:** WebSockets provide persistent, full-duplex communication channels over a single TCP connection, enabling real-time, low-latency message exchange necessary for instant chat applications.
9.  **9. Each HTTP request is independent and unrelated to previous or subsequent requests; the server retains no memory of past interactions with a client.** - **Concept:** HTTP Overview (Statelessness). **Reason:** Statelessness means that the server treats every request as if it's new, without relying on any stored information from prior requests in the current session.
10. **10. `GET`** - **Concept:** HTTP Request Methods. **Reason:** The `GET` method is designed to retrieve information and is defined as both "safe" (no side effects on the server) and "idempotent" (multiple identical requests have the same effect as one) according to HTTP specifications.

### Section 2: Reasoning Questions - Answers
1.  **1. Explanation:** Packet switching breaks data into small, independent packets that can travel different routes and be reassembled at the destination. This contrasts with circuit switching's dedicated, end-to-end connection. **Concept:** Packet Switching vs. Circuit Switching. **Reason:** Packet switching offers greater resilience because if one path fails, packets can be rerouted, ensuring communication continuity. It's also more efficient as network resources are shared and not reserved, leading to better utilization and less idle time.
2.  **2. Explanation:** Internet Standards are crucial for:
    1)  **Interoperability:** They ensure that diverse hardware and software from different manufacturers can communicate and work together seamlessly, allowing a truly global network.
    2)  **Innovation and Competition:** By providing a common foundation, standards prevent vendor lock-in and foster innovation, as new technologies can be built upon established protocols without needing to recreate fundamental communication methods. This promotes a healthy competitive ecosystem.
    **Concept:** Importance of Internet Standards. **Reason:** Without common standards, the internet would be a fragmented collection of incompatible networks, hindering global communication and technological progress.
3.  **3. Explanation:** The Internet is the global physical infrastructure—the network of interconnected computers, cables, and routers—that allows data exchange. The World Wide Web, however, is a collection of interconnected documents and other web resources, linked by hyperlinks and URLs, accessed via HTTP and viewed with web browsers. **Concept:** Internet vs. WWW. **Reason:** The Web is an application that runs *on* the Internet, not the Internet itself. One is the infrastructure, the other is a service built upon it.
4.  **4. Explanation:** When a user enters a URL, the web browser (client) first uses DNS to resolve the domain name to an IP address. Then, the client establishes a TCP connection to the web server at that IP address. The browser then sends an HTTP request (e.g., GET for a page). The web server receives the request, locates the requested resource, and sends an HTTP response containing the resource (e.g., HTML, CSS, JavaScript) back to the browser. Finally, the browser renders these assets to display the web page to the user. **Concept:** WWW Architecture (Client-Server Model). **Reason:** This step-by-step process ensures that the client can correctly identify, connect to, request from, and receive content from the server to display the web page.
5.  **5. Explanation:** If an email client is configured to use POP3 with its default "download-and-delete" setting, emails will be downloaded to that specific device and then removed from the mail server immediately or after a short grace period. **Concept:** POP3 Implications. **Reason:** This means those emails will no longer be accessible from any other device or a webmail interface. While some clients offer an option to "leave a copy on the server," the core POP3 design is geared towards single-device access, making multi-device synchronization challenging and potentially leading to inconsistent mailbox states across devices.
6.  **6. Explanation:** Standard FTP transmits data, including usernames, passwords, and file contents, in plain text over the network. This makes it highly vulnerable to eavesdropping (sniffing), where an attacker can easily intercept and read sensitive information. Additionally, data integrity cannot be guaranteed. **Concept:** FTP Security. **Reason:** Alternatives should include **SFTP (SSH File Transfer Protocol)**, which encrypts the entire communication channel using SSH, or **FTPS (FTP over SSL/TLS)**, which adds an SSL/TLS layer for encryption, significantly enhancing security.
7.  **7. Explanation:** In HTTP/1.1, pipelining could send multiple requests, but responses had to be received in order, leading to "head-of-line blocking" if one response was delayed. **Concept:** HTTP/2 Multiplexing. **Reason:** HTTP/2's multiplexing allows multiple requests and responses to be interleaved and flow concurrently over a *single* TCP connection, each carried on its own independent stream. This eliminates head-of-line blocking at the application level, as a slow response for one resource does not block the delivery of others, thus making more efficient use of the network and improving page load times.
8.  **8. Explanation:** The `POST` method is generally considered neither safe nor idempotent. It's not "safe" because it is intended to cause a side-effect on the server (e.g., creating a new resource, submitting form data that changes server state). **Concept:** HTTP Methods (Idempotence and Safety). **Reason:** It's not "idempotent" because repeatedly sending the same `POST` request (e.g., submitting an order form multiple times) will typically result in multiple distinct actions or creations on the server, rather than having the same effect as a single successful request.
9.  **9. Explanation:** When a user submits a registration form, the data is sent via an HTTP POST request to the server. A server-side script (e.g., PHP, Node.js, Python) on the web server receives this data. This script would then validate the input, interact with a database (e.g., MySQL, MongoDB) to store the new user's credentials and profile information, and then generate a dynamic HTML response. **Concept:** Server-Side Scripting. **Reason:** This response could include a personalized success message confirming the account creation, relevant user data, or a redirect to a user dashboard, all rendered specifically for the newly registered user, demonstrating the server's role in processing and personalizing content.
10. **10. Explanation:** AJAX (Asynchronous JavaScript and XML/JSON) is fundamental to this experience. As the user scrolls, JavaScript code in the browser detects reaching the end of the current feed. This triggers an asynchronous HTTP request (an AJAX request) to the server in the background, without reloading the entire page. The server responds with new post data (often in JSON format). **Concept:** AJAX, Dynamic Web Pages, Client-Side Scripting. **Reason:** JavaScript then takes this new data and dynamically adds new HTML elements to the existing page's DOM, seamlessly appending the new posts to the feed, making the experience fluid and responsive without interrupting the user's interaction.

### Section 3: Real-World Cases - Answers
1.  **1. Case: E-commerce Checkout**
    *   **HTTP Method:** `POST`.
    *   **Concept:** HTTP Request Methods, Safe/Idempotent.
    *   **Reason:** `POST` is used because placing an order involves creating a new resource (the order itself) and modifying the state of the server (e.g., updating inventory, recording the transaction). Since `POST` is designed for submitting data that causes side-effects and is not idempotent, it is appropriate for non-repeatable actions like confirming an order, ensuring that clicking "Place Order" multiple times doesn't create multiple orders.
2.  **2. Case: Video Streaming Site**
    *   **Explanation:** The initial quick load is typically for the static (or dynamically generated, but small) HTML, CSS, and JavaScript of the web page interface. These are relatively small files transferred quickly via HTTP (or HTTP/2/3). The video content, however, is a much larger data stream. After the page loads, the browser makes a separate request for the video. **Concept:** HTTP Request/Response, Data Transfer, Bandwidth, Dynamic Content. **Reason:** The buffering occurs because the network bandwidth or the server's streaming capacity is insufficient to deliver the large video file instantly at playback speed, requiring a segment of the video to download and store locally before playback can begin smoothly. This highlights the difference in scale between a webpage's assets and multimedia content.
3.  **3. Case: Company-Internal Wiki**
    *   **Type of Web Page Generation:** Dynamic web pages.
    *   **Concept:** Static vs. Dynamic Web Pages, Server-Side Scripting, Client-Side Scripting, Databases.
    *   **Reason:** Allowing direct editing requires dynamic web pages because the content of the wiki needs to be stored, retrieved, and updated in real-time.
    *   **Technologies Involved:**
        -   **Server-Side Scripting:** (e.g., Python with Flask, PHP, Node.js with Express) would be needed to handle user authentication, process submitted edits, save changes to the database, and dynamically generate the HTML for viewing or editing pages.
        -   **Database:** (e.g., SQLite, PostgreSQL) would store the wiki content, user accounts, and possibly version history for pages.
        -   **Client-Side Scripting:** (JavaScript) would enhance the editing experience (e.g., rich text editor functionality, real-time preview, form validation) and might use AJAX to submit changes or load content without full page reloads.
4.  **4. Case: Email Synchronization**
    *   **Protocol:** IMAP (Internet Message Access Protocol).
    *   **Concept:** POP3 vs. IMAP.
    *   **Reason:** IMAP is designed to keep messages on the mail server and synchronize the mailbox state (read/unread, deleted, moved to folders) across all connected devices. Unlike POP3's default "download-and-delete" model, IMAP acts as a remote file server for email, ensuring that the view of your mailbox is consistent regardless of which device you use, making it ideal for multi-device access and synchronization.
5.  **5. Case: Online Gaming Chat**
    *   **Communication Model:** Primarily **client-server**, possibly with some P2P aspects for specific game data but centralized for chat.
    *   **Underlying Technology:** **WebSockets**.
    *   **Concept:** Chat Technologies, Real-time Communication, WebSockets.
    *   **Reason:** For instant, low-latency, and reliable group messaging, a client-server model with **WebSockets** is highly efficient. Players (clients) maintain a persistent WebSocket connection to a central chat server. Messages sent by one player are rapidly broadcast by the server to all other players connected to the same chat room via their open WebSocket connections. WebSockets are ideal because they provide a full-duplex, sticky connection, avoiding the overhead of repeated HTTP requests and enabling true push notifications from the server to clients, which is critical for real-time responsiveness in gaming chat. While P2P might offer privacy, the complexity of managing group chats and offline messages in a real-time game environment makes a server-driven WebSocket approach more practical and performant.
6.  **6. Case: Broken Image Link**
    *   **HTTP Status Code:** `404 Not Found`.
    *   **Concept:** HTTP Status Codes (Client Error).
    *   **Reason:** A `404 Not Found` status code indicates that the web server successfully received the HTTP request for the image but was unable to locate the resource at the specified URL. This is the most common reason for a broken image icon, implying either a typo in the image's URL, the image file being moved, or deleted from the server.
7.  **7. Case: Website Migration**
    *   **HTTP Status Code:** `301 Moved Permanently`.
    *   **Concept:** HTTP Status Codes (Redirection).
    *   **Reason:** The `301 Moved Permanently` status code is crucial for permanent URL redirection. When a browser or search engine receives a `301` response from `oldblog.com`, it understands that the resource has permanently moved to `newblog.com`. Browsers will automatically redirect users to the new URL, and search engines will update their indexes to reflect the new location, preserving SEO value and ensuring old links don't break.
8.  **8. Case: Large File Upload**
    *   **Most Appropriate Protocol:** SFTP (SSH File Transfer Protocol) or HTTP with robust upload mechanisms (like `PUT` or `POST` for multipart uploads and resumable uploads).
    *   **Concept:** File Transfer Protocols, Security, HTTP Methods.
    *   **Reason:**
        -   **Standard FTP** is a poor choice due to its lack of encryption, making it insecure for sensitive data like video files (which might contain personal content).
        -   **SFTP** is a strong candidate because it provides secure, encrypted file transfers over an SSH tunnel, suitable for any file size and sensitive data.
        -   While **HTTP `POST`** or **`PUT`** are commonly used for uploads in web applications, they need to be implemented with features like resumable uploads and progress indicators for *very large* files to be efficient and user-friendly. Modern cloud services often build their sophisticated upload mechanisms on top of HTTPS (`PUT`/`POST`) with custom APIs, offering robust security and reliability for large file chunks, often overcoming the "stateless" nature with session management. For raw file transfer, especially for non-web interfaces, SFTP is often preferred for its built-in reliability and security. If the upload is via a web browser, HTTPS (`PUT`/`POST`) would be the standard.
9.  **9. Case: Social Media Feed Update**
    *   **Explanation:** AJAX (Asynchronous JavaScript and XML/JSON) is fundamental to this experience. As the user scrolls, JavaScript code in the browser detects reaching the end of the current feed. This triggers an asynchronous HTTP request (an AJAX request) to the server in the background, without reloading the entire page. The server responds with new post data (often in JSON format). **Concept:** AJAX, Dynamic Web Pages, Client-Side Scripting. **Reason:** JavaScript then takes this new data and dynamically adds new HTML elements to the existing page's DOM, seamlessly appending the new posts to the feed, making the experience fluid and responsive without interrupting the user's interaction.
10. **10. Case: International Website Access**
    *   **Contribution to UX:** The `Accept-Language` header allows the web server to detect the user's preferred language(s) and, if available, serve a localized version of the website content (e.g., text, currency, date formats) tailored to that language. This significantly enhances the user experience by making the content more accessible and relevant without the user having to manually select a language.
    *   **Part of HTTP Request:** It is a **Request Header**.
    *   **Concept:** HTTP Request Headers, Localization. **Reason:** `Accept-Language` is a standard HTTP request header sent by the client (browser) to inform the server of the human languages that are preferred in the response to the request.

### Section 4: Rapid Fire Questions - Answers
1.  **1. What does `RFC` stand for?** Requests for Comments.
2.  **2. Who invented the World Wide Web?** Tim Berners-Lee.
3.  **3. Is HTTP/1.1 a stateful or stateless protocol?** Stateless.
4.  **4. Which HTTP method is generally used for creating new resources on a server?** `POST` (or `PUT` if the resource ID is known and client-generated).
5.  **5. What is the default unencrypted port for SMTP?** Port 25.
6.  **6. Which FTP mode helps overcome client-side firewall issues?** Passive Mode.
7.  **7. What is the purpose of a URI?** To uniquely identify a resource on the web.
8.  **8. Name a server-side scripting language mentioned in Unit I.** PHP (or Node.js, Python, ASP.NET, JSP).
9.  **9. What port does HTTPS typically use?** Port 443.
10. **10. What was the name of the precursor to the internet developed in the 1960s?** ARPANET.

### Section 5: All Possible 2-Mark Remember Questions - Answers
1.  **1. What is a computer network?** - **Concept:** Definition of Network. **Reason:** A computer network is a collection of interconnected autonomous devices that exchange data to share resources and facilitate communication.
2.  **2. Differentiate between packet switching and circuit switching.** - **Concept:** Network Communication Methods. **Reason:** Packet switching breaks data into independent packets for flexible routing, while circuit switching establishes a dedicated, continuous connection for the duration of communication.
3.  **3. What was the significance of ARPANET?** - **Concept:** History of Internet. **Reason:** ARPANET was the precursor to the modern internet and the first large-scale network to successfully implement packet switching, proving its viability for creating a decentralized and resilient network.
4.  **4. List two examples of end devices and two examples of intermediary devices.** - **Concept:** Network Components. **Reason:** End devices: PC, Smartphone. Intermediary devices: Router, Switch.
5.  **5. What is the purpose of an Internet Standard?** - **Concept:** Role of Standards. **Reason:** To ensure interoperability between different systems and devices on the internet, allowing them to communicate seamlessly regardless of the manufacturer.
6.  **6. Name two major internet standards organizations and their primary focus.** - **Concept:** Standards Bodies. **Reason:** The IETF (Internet Engineering Task Force) focuses on core internet protocols (like TCP/IP). The W3C (World Wide Web Consortium) focuses on web technologies (like HTML and CSS).
7.  **7. What is an RFC?** - **Concept:** IETF Publications. **Reason:** An RFC (Request for Comments) is a publication from the IETF that describes methods, behaviors, research, or innovations applicable to the working of the internet. Some RFCs become Internet Standards.
8.  **8. Why is interoperability important?** - **Concept:** Benefits of Standards. **Reason:** Interoperability allows hardware and software from different vendors to work together, which fosters competition, prevents market monopolies, and provides a consistent user experience.
9.  **9. Distinguish between the Internet and the World Wide Web.** - **Concept:** Internet vs. Web. **Reason:** The Internet is the global physical network of computers (hardware infrastructure), while the World Wide Web is a system of interlinked documents and applications that runs on top of the Internet (software system).
10. **10. Who invented the World Wide Web?** - **Concept:** Web History. **Reason:** The WWW was invented by Tim Berners-Lee in 1989 at CERN.
11. **11. List the three foundational technologies of the Web.** - **Concept:** Web Fundamentals. **Reason:** HTML (HyperText Markup Language), URI (Uniform Resource Identifier), and HTTP (HyperText Transfer Protocol).
12. **12. What is a URL?** - **Concept:** Resource Identification. **Reason:** A URL (Uniform Resource Locator) is a specific type of URI that provides the unique address of a resource on the Web and the protocol to retrieve it.
13. **13. Explain the client-server model in the context of the WWW.** - **Concept:** WWW Architecture. **Reason:** In the WWW client-server model, web browsers act as clients requesting resources (like web pages) from web servers, which store and deliver those resources.
14. **14. What is the primary role of a web browser?** - **Concept:** Client Role. **Reason:** To request, interpret, and render web content (HTML, CSS, JavaScript) received from web servers, displaying it to the user.
15. **15. List two key functions of a web server.** - **Concept:** Server Role. **Reason:** Listening for HTTP requests from clients and sending HTTP responses containing the requested web resources.
16. **16. How do HTTP, HTML, and URI collectively enable the WWW architecture?** - **Concept:** Web Integration. **Reason:** A URI (URL) specifies *where* a resource is. HTTP is the *protocol* used to request and transfer that resource. HTML is the *language* used to structure the content of the resource itself.
17. **17. What is the primary function of SMTP?** - **Concept:** Email Sending. **Reason:** SMTP (Simple Mail Transfer Protocol) is used for sending and transferring email messages between mail servers.
18. **18. Name the four main components of an email system.** - **Concept:** Email Architecture. **Reason:** User Agent (MUA), Mail Submission Agent (MSA), Mail Transfer Agent (MTA), and Mail Delivery Agent (MDA).
19. **19. Which port is commonly used for client mail submission with encryption?** - **Concept:** SMTP Ports. **Reason:** Port 587.
20. **20. What does the `DATA` command signify in an SMTP session?** - **Concept:** SMTP Commands. **Reason:** It signifies that the client is about to send the actual content (headers and body) of the email message.
21. **21. What is the primary function of POP3?** - **Concept:** Email Retrieval. **Reason:** POP3 (Post Office Protocol version 3) is used by email clients to retrieve email messages from a mail server.
22. **22. Describe the "download-and-delete" model of POP3.** - **Concept:** POP3 Functionality. **Reason:** In this model, when an email client retrieves messages using POP3, it typically downloads them to the local device and then deletes them from the mail server.
23. **23. Which port is used for secure POP3 connections?** - **Concept:** POP3 Ports. **Reason:** Port 995 (POP3S).
24. **24. State one key difference between POP3 and IMAP.** - **Concept:** Email Protocols Comparison. **Reason:** POP3 typically downloads messages and removes them from the server, while IMAP keeps messages on the server and synchronizes their state across multiple devices.
25. **25. What is the primary purpose of FTP?** - **Concept:** File Transfer. **Reason:** FTP (File Transfer Protocol) is used for transferring files between a client and a server on a computer network.
26. **26. Explain the two types of connections used by FTP.** - **Concept:** FTP Architecture. **Reason:** FTP uses a control connection (for commands and responses, typically on port 21) and a data connection (for actual file transfer, typically on port 20 or dynamic).
27. **27. Differentiate between active and passive FTP modes.** - **Concept:** FTP Modes. **Reason:** In active mode, the server initiates the data connection to the client. In passive mode, the client initiates both the control and data connections to the server.
28. **28. Why is standard FTP considered insecure?** - **Concept:** FTP Security. **Reason:** Standard FTP transmits data, including authentication credentials, in plain text, making it vulnerable to interception.
29. **29. What is the primary characteristic that distinguishes chat from email?** - **Concept:** Chat vs. Email. **Reason:** Chat provides real-time, synchronous communication, allowing for immediate exchange of messages, unlike the asynchronous nature of email.
30. **30. Name an early chat protocol and one of its key features.** - **Concept:** Chat History. **Reason:** Internet Relay Chat (IRC) is an early chat protocol, known for its use of "channels" (chat rooms) for group communication.
31. **31. What is the main advantage of using WebSockets for modern web-based chat?** - **Concept:** Real-time Web. **Reason:** WebSockets enable real-time, full-duplex communication over a single, persistent TCP connection, allowing for instant message delivery without constant polling.
32. **32. Briefly explain a privacy concern associated with client-server chat models.** - **Concept:** Chat Security. **Reason:** In a client-server model, messages typically pass through central servers, which could potentially store or access message content, raising privacy concerns.
33. **33. What does "stateless" mean in the context of HTTP?** - **Concept:** HTTP Characteristics. **Reason:** HTTP is stateless because each request from a client to a server is treated as an independent transaction, with the server retaining no memory of previous requests from that client.
34. **34. Name two key improvements introduced in HTTP/1.1 over HTTP/1.0.** - **Concept:** HTTP Evolution. **Reason:** HTTP/1.1 introduced persistent connections (keep-alive) and pipelining, significantly reducing overhead by allowing multiple requests over a single TCP connection.
35. **35. What is the main advantage of HTTP/2's multiplexing feature?** - **Concept:** HTTP/2 Performance. **Reason:** Multiplexing allows multiple requests and responses to be interleaved over a single TCP connection without head-of-line blocking, improving web page load times.
36. **36. Briefly explain the difference between HTTP and HTTPS.** - **Concept:** Web Security. **Reason:** HTTPS is the secure version of HTTP, using SSL/TLS encryption to protect data transferred between a client and server, ensuring privacy and data integrity.
37. **37. List the three main parts of an HTTP request.** - **Concept:** HTTP Request Structure. **Reason:** Request Line, Request Headers, and (optional) Request Body.
38. **38. What is the purpose of the `GET` HTTP method?** - **Concept:** HTTP Methods. **Reason:** The `GET` method is used to request data from a specified resource and should only retrieve data without altering server state.
39. **39. What does an HTTP status code of `200 OK` signify?** - **Concept:** HTTP Status Codes. **Reason:** It signifies that the HTTP request was successful, and the server has provided the requested resource.
40. **40. Give an example of a `4xx` status code and its meaning.** - **Concept:** HTTP Error Codes. **Reason:** `404 Not Found` indicates that the server cannot find the requested resource.
41. **41. What is the primary difference between a static and a dynamic web page?** - **Concept:** Web Page Types. **Reason:** Static web pages have fixed, pre-written content, while dynamic web pages generate content on the fly based on server-side logic and data.
42. **42. Name two popular server-side scripting languages/frameworks used for dynamic web page generation.** - **Concept:** Server-Side Technologies. **Reason:** PHP, Node.js (with Express.js), Python (with Django/Flask), ASP.NET, JSP.
43. **43. What is the role of a database in generating dynamic web pages?** - **Concept:** Dynamic Web Components. **Reason:** Databases store and manage the variable data (e.g., user profiles, product listings) that server-side scripts retrieve and use to construct dynamic web content.
44. **44. How does AJAX enhance the user experience of dynamic web pages?** - **Concept:** Client-Side Dynamism. **Reason:** AJAX allows parts of a web page to be updated asynchronously without requiring a full page reload, leading to a faster and more responsive user experience.