---
title: "Unit I: File Transfer Protocol (FTP)"
id: unit1-topic7-ftp
tags:
  - unit-1
  - ftp
  - file-transfer
  - application-layer
  - client-server
aliases:
  - "FTP"
links:
  - "[[UITx/Unit_01_Topic_06_POP3.md|POP3]]"
  - "[[UITx/Unit_01_Topic_08_Chat.md|Chat]]"
---

# Unit I, Topic 7: File Transfer Protocol (FTP)

> [!quote] In the digital realm, the exchange of files is as fundamental as the exchange of words. The File Transfer Protocol (FTP) is the ancient, yet enduring, method for moving digital artifacts across the network, a testament to its robust design. Let us now explore this venerable protocol.

## 1. What is FTP?

**FTP (File Transfer Protocol)** is a standard network protocol used for the transfer of computer files between a client and server on a computer network. FTP is built on a client-server model architecture and uses separate control and data connections between the client and the server.

Its primary purpose is to enable users to:
-   Upload files from their local computer to a server.
-   Download files from a server to their local computer.
-   Manage files on a remote server (e.g., list directories, rename, delete).

FTP is one of the oldest protocols still in use on the internet, predating HTTP and the World Wide Web.

## 2. FTP Architecture: Dual Connections

A unique characteristic of FTP is its use of **two separate connections** between the client and the server:

1.  **Control Connection:**
    -   Used for sending commands (e.g., `USER`, `PASS`, `LIST`, `RETR`, `STOR`) and receiving responses (e.g., `200 OK`, `550 File not found`).
    -   Remains open for the entire duration of the FTP session.
    -   Uses **TCP Port 21** by default.

2.  **Data Connection:**
    -   Used for the actual transfer of file data and directory listings.
    -   Is opened and closed for each file transfer or directory listing.
    -   Uses **TCP Port 20** by default for active mode, or a dynamically assigned port for passive mode.

```
+-----------------+                       +-----------------+
|   FTP Client    |                       |   FTP Server    |
| (e.g., FileZilla)|                       | (e.g., vsftpd)  |
+-----------------+                       +-----------------+
        |                                         |
        |--- Control Connection (Port 21) ------->| (Commands & Responses)
        |                                         |
        |--- Data Connection (Port 20 or dynamic)>| (File Data & Listings)
        |                                         |
```

## 3. FTP Modes: Active vs. Passive

The way the data connection is established defines whether FTP operates in **active** or **passive** mode. This distinction is crucial, especially when firewalls are involved.

### a) Active Mode FTP

In active mode:
1.  The client establishes the **control connection** from a random port to server port 21.
2.  The client sends its IP address and a random port number to the server via the control connection, telling the server where to connect for the data connection.
3.  The server then initiates the **data connection** from its port 20 to the client's specified IP address and port.

```
+-----------------+                       +-----------------+
|   FTP Client    |                       |   FTP Server    |
+-----------------+                       +-----------------+
        |                                         |
        |  Client_Port_X -> Server_Port_21 (Control)  |
        |---------------------------------------->|
        |                                         |
        |  Client_Port_X <- Server_Port_20 (Data)   |
        |<----------------------------------------|
```

**Problem with Active Mode:** Many clients are behind firewalls that block incoming connections. Since the server tries to initiate the data connection *to* the client, active mode often fails if the client's firewall is not configured to allow this.

### b) Passive Mode FTP

Passive mode was developed to address the firewall issues of active mode.

In passive mode:
1.  The client establishes the **control connection** from a random port to server port 21.
2.  The client sends a `PASV` command to the server.
3.  The server responds with its IP address and a random port number (ephemeral port) that it has opened for the data connection.
4.  The client then initiates the **data connection** from another random port to the server's specified IP address and random port.

```
+-----------------+                       +-----------------+
|   FTP Client    |                       |   FTP Server    |
+-----------------+                       +-----------------+
        |                                         |
        |  Client_Port_X -> Server_Port_21 (Control)  |
        |---------------------------------------->|
        |                                         |
        |  Client_Port_Y -> Server_Port_Z (Data)    |
        |---------------------------------------->|
```

**Advantage of Passive Mode:** Since the client initiates both the control and data connections, it works much better through client-side firewalls, as outgoing connections are typically allowed. Passive mode is the default and preferred mode for most modern FTP clients.

## 4. FTP Commands and Responses

FTP uses a set of standard commands and numeric response codes.

**Common FTP Commands (from client to server via control connection):**
-   `USER [username]`: Specifies the username for authentication.
-   `PASS [password]`: Specifies the password for authentication.
-   `CWD [directory]`: Change working directory.
-   `LIST`: Returns a list of files in the current directory.
-   `RETR [filename]`: Retrieve (download) a file.
-   `STOR [filename]`: Store (upload) a file.
-   `DELE [filename]`: Delete a file.
-   `QUIT`: Terminate the FTP session.
-   `PORT [h1,h2,h3,h4,p1,p2]`: Used in active mode to tell the server the client's IP and port for the data connection.
-   `PASV`: Used in passive mode to request the server to open a data port.

**Common FTP Response Codes (from server to client via control connection):**
-   `200 Command okay`: The command was successful.
-   `220 Service ready for new user`: Server is ready.
-   `221 Service closing control connection`: Server is shutting down.
-   `227 Entering Passive Mode (h1,h2,h3,h4,p1,p2)`: Server's response to `PASV`, providing IP and port for data connection.
-   `230 User logged in, proceed`: Authentication successful.
-   `425 Can't open data connection`: Data connection failed.
-   `530 Not logged in`: Authentication required.
-   `550 Requested action not taken: file unavailable`: File not found or access denied.

## 5. Security Considerations: SFTP and FTPS

Standard FTP transmits data, including usernames and passwords, in plain text, making it vulnerable to eavesdropping. To address this, secure alternatives have been developed:

-   **SFTP (SSH File Transfer Protocol):** Not directly related to FTP, but a separate protocol that runs over SSH (Secure Shell). It encrypts both commands and data.
-   **FTPS (FTP Secure):** FTP over SSL/TLS. It adds an SSL/TLS layer to encrypt FTP communication.

## 6. Exam-Oriented Insights

FTP's dual-connection architecture and modes are key concepts.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the primary purpose of FTP?**
>     *Answer:* FTP (File Transfer Protocol) is used for transferring files between a client and a server on a computer network.
> 2.  **Explain the two types of connections used by FTP.**
>     *Answer:* FTP uses a control connection (for commands and responses, typically on port 21) and a data connection (for actual file transfer, typically on port 20 or dynamic).
> 3.  **Differentiate between active and passive FTP modes.**
>     *Answer:* In active mode, the server initiates the data connection to the client. In passive mode, the client initiates both the control and data connections to the server.
> 4.  **Why is standard FTP considered insecure?**
>     *Answer:* Standard FTP transmits data, including authentication credentials, in plain text, making it vulnerable to interception.

> [!tip] **For Higher Mark Questions:**
> Be prepared to draw a diagram illustrating the dual-connection architecture of FTP. Explain the step-by-step process of a file download using both active and passive modes, highlighting the role of firewalls. Discuss the security vulnerabilities of plain FTP and the solutions offered by SFTP and FTPS.

---

We have now traversed the pathways of the File Transfer Protocol, understanding its dual-connection architecture and the nuances of active and passive modes. This knowledge is fundamental for managing digital assets across networks.
