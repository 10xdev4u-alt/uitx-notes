---
title: "Unit I: Introduction to the World Wide Web (WWW)"
id: unit1-topic3-intro-www
tags:
  - unit-1
  - www
  - http
  - html
  - uri
  - tim-berners-lee
aliases:
  - "The Web"
  - "Intro to WWW"
links:
  - "[[UITx/Unit_01_Topic_02_Internet_Standards.md|Internet Standards]]"
  - "[[UITx/Unit_01_Topic_04_WWW_Architecture.md|WWW Architecture]]"
---

# Unit I, Topic 3: Introduction to the World Wide Web (WWW)

> [!quote] The internet is the network of roads, but the World Wide Web is the universe of destinations—the cities, libraries, and marketplaces you can visit. Let us now explore this world of information, a creation of profound vision.

## 1. The Internet vs. The World Wide Web: A Crucial Distinction

It is a common mistake to use the terms "Internet" and "World Wide Web" (or "the Web") interchangeably. They are, however, fundamentally different.

- **The Internet** is the **hardware**. It is the global network of interconnected computers we have discussed—the physical infrastructure of cables, routers, and servers that allows data to be exchanged. It is the plumbing.
- **The World Wide Web** is the **software**. It is a system of interlinked documents and applications that runs *on top of* the internet. It is the water flowing through the plumbing.

You use the Internet to access the Web. Other services also run on the internet, such as email (SMTP), file transfers (FTP), and chat applications, which are not part of the WWW.

```
+---------------------------------------------------+
|                 Applications Layer                |
| +-------+   +-------+   +-------+   +-----------+ |
| |  WWW  |   | Email |   |  FTP  |   | Other...  | |
| +-------+   +-------+   +-------+   +-----------+ |
+---------------------------------------------------+
|           The Internet (Infrastructure)           |
| (TCP/IP, Routers, Cables, Satellites, etc.)       |
+---------------------------------------------------+
```

## 2. The Architect of the Web: Tim Berners-Lee

The World Wide Web was invented by British scientist **Tim Berners-Lee** in 1989 while working at **CERN**, the European Organization for Nuclear Research.

His goal was to solve a problem: scientists from around the world needed a way to share and manage information and research documents across different types of computers and networks. He envisioned a "web" of information where documents could be easily linked and accessed.

To bring this vision to life, he created three foundational technologies that remain the pillars of the Web today.

## 3. The Three Foundational Technologies of the Web

### a) HTML (HyperText Markup Language)

**Hypertext** is text that contains links (hyperlinks) to other texts. Berners-Lee needed a simple language to create these documents. He developed **HTML**, a markup language used to structure the content of a web page.

- It is not a programming language; it doesn't perform logic.
- It uses **tags** to define elements like headings, paragraphs, images, and, most importantly, hyperlinks.

**Example of simple HTML:**
```html
<!DOCTYPE html>
<html>
<head>
  <title>My First Web Page</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is a paragraph.</p>
  <a href="https://www.example.com">This is a link</a>
</body>
</html>
```
This simple text file, when opened in a web browser, is rendered into a formatted page.

### b) URI (Uniform Resource Identifier)

To link to a document, you need a unique address for it. Berners-Lee created the concept of a **URI**. A URI is a unique string of characters that identifies a resource on the web. The most common type of URI is a **URL (Uniform Resource Locator)**.

A URL provides the "address" of a resource and implies the mechanism to retrieve it.

**Anatomy of a URL:**
```
  https://www.example.com:443/path/to/myfile.html?key1=value1#section1
  \______/ \_____________/ \___/ \________________/ \____________/ \_______/
     |           |          |           |                |            |
  Scheme      Domain      Port         Path            Query      Fragment
           (Host)
```
- **Scheme:** The protocol to use (e.g., `https`, `http`, `ftp`).
- **Domain (Host):** The human-readable name of the server where the resource lives (e.g., `www.example.com`).
- **Port:** The specific "gate" on the server to connect to. `80` is the default for HTTP, `443` for HTTPS.
- **Path:** The specific location of the resource on the server.
- **Query:** Optional parameters sent to the server (e.g., for a search).
- **Fragment:** A link to a specific part of the resource itself.

### c) HTTP (HyperText Transfer Protocol)

Finally, a protocol was needed to transfer these hypertext documents across the internet. Berners-Lee defined **HTTP**.

- **HTTP** is the protocol of the Web. It's a request-response protocol that defines how web browsers (clients) request web pages from servers and how servers respond with the content.
- When you type a URL into your browser, it sends an **HTTP request** to the server. The server then processes the request and sends back an **HTTP response**, which typically contains the HTML of the requested page.

## 4. Exam-Oriented Insights

This topic is fundamental to the entire course.

> [!question] **Potential 2-Mark Questions:**
> 1.  **Distinguish between the Internet and the World Wide Web.**
>     *Answer:* The Internet is the global physical network of computers (hardware infrastructure), while the World Wide Web is a system of interlinked documents and applications that runs on top of the Internet (software system).
> 2.  **Who invented the World Wide Web?**
>     *Answer:* The WWW was invented by Tim Berners-Lee in 1989 at CERN.
> 3.  **List the three foundational technologies of the Web.**
>     *Answer:* HTML (HyperText Markup Language), URI (Uniform Resource Identifier), and HTTP (HyperText Transfer Protocol).
> 4.  **What is a URL?**
>     *Answer:* A URL (Uniform Resource Locator) is a specific type of URI that provides the unique address of a resource on the Web and the protocol to retrieve it.

> [!tip] **For Higher Mark Questions:**
> Be prepared to explain the relationship between the Internet and the Web with a clear analogy (e.g., roads vs. houses). For each of the three foundational technologies (HTML, URI, HTTP), explain its specific role and how they work together. For example: "A browser uses a **URL** (the address) to send an **HTTP** request (the message) to a server to fetch a document written in **HTML** (the content)." Drawing a diagram of the URL components is also a common question.

---

We have now demystified the World Wide Web, distinguishing it from the internet and honoring its creator by understanding its three core pillars. This knowledge is the gateway to everything that follows.
