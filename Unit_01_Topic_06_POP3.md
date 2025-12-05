---
title: "Unit I: Post Office Protocol 3 (POP3)"
id: unit1-topic6-pop3
tags:
  - unit-1
  - pop3
  - email
  - mail-protocol
  - application-layer
aliases:
  - "Email Retrieval"
links:
  - "[[UITx/Unit_01_Topic_05_SMTP.md|SMTP]]"
  - "[[UITx/Unit_01_Topic_07_File_Transfer_Protocol.md|File Transfer Protocol]]"
---

# Unit I, Topic 6: Post Office Protocol 3 (POP3)

> [!quote] If SMTP is the diligent courier delivering mail to your digital mailbox, then POP3 is the postman who empties that mailbox, bringing its contents directly to your hands. Let us now understand this protocol, which allows us to retrieve our electronic correspondence.

## 1. What is POP3?

**POP3 (Post Office Protocol version 3)** is an application-layer protocol used by email clients to retrieve email from a mail server. It is designed to be simple and efficient, primarily for users who want to download their emails to a single device and then delete them from the server.

While SMTP handles the sending and transferring of emails between servers, POP3 (along with IMAP, which we'll briefly touch upon) handles the final step: getting the email from the recipient's mail server to their email client (MUA).

## 2. POP3 in the Email Ecosystem

Recall the email flow we discussed with SMTP:

```
+----------+     +-----------------+     +-----------------+     +----------+
| Sender's | --> | Sender's Mail   | --> | Recipient's Mail| --> |Recipient's|
|   MUA    |     | Server (MTA/MSA)|     | Server (MTA/MDA)| --> |   MUA    |
+----------+     +-----------------+     +-----------------+     +----------+
  (Compose &      (Sends via SMTP)      (Receives via SMTP,   (Retrieves via
   Send)                                  Stores in Mailbox)    POP3/IMAP)
```

POP3 specifically governs the last arrow: from the Recipient's Mail Server to the Recipient's MUA.

## 3. How POP3 Works: The Download-and-Delete Model

POP3 operates in a very straightforward manner, often described as a "download-and-delete" model.

### The Three States of a POP3 Session:

1.  **Authorization:** The client connects to the server and provides username and password for authentication.
2.  **Transaction:** The client retrieves messages, marks them for deletion, or gets mail statistics.
3.  **Update:** The server deletes messages marked for deletion.

### POP3 Communication Process (Commands and Responses)

Like SMTP, POP3 is a text-based protocol. The client sends commands, and the server responds with status indicators and data.

**Common POP3 Commands (from client to server):**
-   `USER [username]`: Specifies the username for authentication.
-   `PASS [password]`: Specifies the password for authentication.
-   `STAT`: Requests the number of messages and the total size of the mailbox.
-   `LIST [msg_number]`: Lists message numbers and their sizes. If `msg_number` is provided, lists details for that specific message.
-   `RETR [msg_number]`: Retrieves the specified message.
-   `DELE [msg_number]`: Marks the specified message for deletion. The message is only actually deleted during the `UPDATE` state (after `QUIT`).
-   `NOOP`: No operation (server responds with `+OK`). Used to keep the connection alive.
-   `RSET`: Unmarks all messages marked for deletion.
-   `QUIT`: Terminates the session and enters the `UPDATE` state (deleting marked messages).

**Common POP3 Responses (from server to client):**
-   `+OK`: Command successful.
-   `-ERR`: Command failed or error occurred.

### A Simple POP3 Session Example:

```
Client: (Connects to POP3 server)
Server: +OK POP3 server ready
Client: USER your_username
Server: +OK
Client: PASS your_password
Server: +OK User successfully logged on
Client: STAT
Server: +OK 2 320  (2 messages, total size 320 bytes)
Server: LIST
Server: +OK
Server: 1 120
Server: 2 200
Server: .
Client: RETR 1
Server: +OK 120 octets
Server: (Email content for message 1)
Server: .
Client: DELE 1
Server: +OK Message 1 deleted
Client: QUIT
Server: +OK POP3 server signing off (2 messages left)
```
In this example, message 1 is downloaded and marked for deletion. When `QUIT` is issued, message 1 is permanently removed from the server.

## 4. POP3 vs. IMAP (Internet Message Access Protocol)

While POP3 is simple and downloads messages to a single client, **IMAP** offers a more advanced and flexible approach to email retrieval.

| Feature           | POP3                                       | IMAP                                                              |
| :---------------- | :----------------------------------------- | :---------------------------------------------------------------- |
| **Storage**       | Downloads messages to client, often deletes from server. | Keeps messages on server, synchronizes with client.               |
| **Access**        | Best for single-device access.             | Best for multiple-device access (e.g., phone, laptop, webmail).   |
| **Offline Access**| Full offline access to downloaded messages. | Can access messages offline, but typically downloads on demand.   |
| **Folders**       | Limited server-side folder management.     | Full server-side folder management (create, delete, move messages). |
| **Message State** | No server-side tracking of read/unread.    | Tracks read/unread status, flags, etc., on the server.            |

For modern users accessing email from multiple devices, IMAP is generally preferred. However, POP3 remains relevant for specific use cases, such as archiving emails locally or when server storage is limited.

## 5. POP3 Ports

POP3 typically uses the following TCP ports:
-   **Port 110:** The standard, unencrypted port for POP3.
-   **Port 995:** Used for POP3S (POP3 over SSL/TLS), which provides an encrypted connection for secure email retrieval.

## 6. Exam-Oriented Insights

Understanding POP3's role and its distinction from other protocols is important.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the primary function of POP3?**
>     *Answer:* POP3 (Post Office Protocol version 3) is used by email clients to retrieve email messages from a mail server.
> 2.  **Describe the "download-and-delete" model of POP3.**
>     *Answer:* In this model, when an email client retrieves messages using POP3, it typically downloads them to the local device and then deletes them from the mail server.
> 3.  **Which port is used for secure POP3 connections?**
>     *Answer:* Port 995 (POP3S).
> 4.  **State one key difference between POP3 and IMAP.**
>     *Answer:* POP3 typically downloads messages and removes them from the server, while IMAP keeps messages on the server and synchronizes their state across multiple devices.

> [!tip] **For Higher Mark Questions:**
> Be prepared to explain the three states of a POP3 session (Authorization, Transaction, Update). Outline a simplified POP3 conversation, showing key commands and responses. A common question is to compare and contrast POP3 and IMAP, discussing their advantages and disadvantages for different user scenarios. Emphasize why POP3 might still be used despite IMAP's prevalence.

---

We have now illuminated the workings of POP3, understanding how our email clients retrieve messages from the digital post office. This completes our exploration of the fundamental protocols for electronic mail.
