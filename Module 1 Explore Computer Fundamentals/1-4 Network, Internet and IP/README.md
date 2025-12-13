# 🌐 Network, Internet and IP - Core Concepts

## 1. What is the Internet?

The **Internet** (or **"the Net"**) is a massive, global network of interconnected computer networks. It uses the standard **Internet Protocol Suite (TCP/IP)** to communicate between networks and devices.

- It is a network of networks that links billions of devices worldwide.
- It facilitates a wide variety of information and communication services, including the World Wide Web (WWW), email, file sharing, and video streaming.
- It is built on top of a hierarchical, tiered structure of private, public, academic, business, and government networks, connected by a vast array of electronic, wireless, and optical networking technologies.

## 2. What is an IP Address?

An **IP (Internet Protocol) Address** is a numerical label assigned to every device connected to a computer network that uses the Internet Protocol for communication.

- **Identification:** It serves two main functions: **host or network interface identification** and **location addressing**. It tells the network _where_ a device is.
- **Analogy:** Think of it as a **digital street address** for your computer, allowing data (like a letter) to be routed and delivered to the correct destination.

### IPv4 vs. IPv6

There are currently two versions of the Internet Protocol in use: IPv4 and IPv6. IPv6 was developed primarily to deal with the exhaustion of available IPv4 addresses.

| Feature             | **IPv4 (Internet Protocol version 4)**                | **IPv6 (Internet Protocol version 6)**                                                      |
| :------------------ | :---------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| **Address Size**    | 32-bit (Offers $\approx 4.3$ billion addresses)       | 128-bit (Offers $3.4 \times 10^{38}$ addresses)                                             |
| **Address Format**  | Dotted Decimal Notation (e.g., `192.168.1.1`)         | Hexadecimal Notation, separated by colons (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`) |
| **Header Checksum** | Yes, the router checks and recalculates it.           | No, relies on Link-Layer error detection.                                                   |
| **Configuration**   | Manual or DHCP (Dynamic Host Configuration Protocol). | Auto-configuration is built-in.                                                             |
| **Security**        | Security features (IPsec) are optional.               | Security features (IPsec) are mandatory.                                                    |
| **Mobile**          | Limited mobility features.                            | Built-in mobility support.                                                                  |

## 3. What is a URL?

A **URL (Uniform Resource Locator)** is a reference (an address) to a resource on the Internet. It is the mechanism used by web browsers and other software to retrieve resources.

A typical URL is structured as:

$$
\text{Scheme}://\text{Subdomain.Domain.TopLevelDomain}[:\text{Port}]/\text{Path}/\text{File}
$$

**Example:** `https://www.google.com/search?q=networking`

| Part                       | Description                                          | Example from URL |
| :------------------------- | :--------------------------------------------------- | :--------------- |
| **Scheme (Protocol)**      | The protocol to be used (e.g., HTTP, HTTPS, FTP).    | `https`          |
| **Domain Name**            | The name of the server hosting the resource.         | `www.google.com` |
| **Top-Level Domain (TLD)** | The highest level in the hierarchical DNS.           | `.com`           |
| **Path/File**              | The specific location of the resource on the server. | `/search`        |
| **Query String**           | Information passed to the server (starts with `?`).  | `q=networking`   |

## 4. What is DNS?

**DNS (Domain Name System)** is a hierarchical and decentralized naming system for computers, services, or any resource connected to the Internet or a private network.

- It is the **Internet's phonebook**. It translates human-readable domain names (like `www.example.com`) into computer-readable IP addresses (like `192.0.2.44`).

### Steps of DNS Resolution

When you type a URL into your browser, the following simplified steps occur for DNS resolution:

1.  **Check Local Cache:** The browser and the operating system (OS) first check their local DNS caches to see if the IP address for the domain is already known.
2.  **Query the Recursive Resolver:** If not found locally, the query is sent to a **DNS Recursive Resolver** (often managed by your ISP).
3.  **Query the Root Server:** The Resolver queries a **Root Name Server** (the top of the DNS hierarchy). The Root Server does not know the IP, but it directs the Resolver to the appropriate **TLD (Top-Level Domain) Name Server** (`.com`, `.org`, etc.).
4.  **Query the TLD Server:** The Resolver queries the TLD Server. It directs the Resolver to the **Authoritative Name Server** for the specific domain (`google.com`).
5.  **Query the Authoritative Name Server:** The Resolver queries the Authoritative Name Server, which holds the actual IP address record for the domain.
6.  **Return the IP:** The Authoritative Name Server sends the IP address back to the Resolver, which then sends it back to your browser.
7.  **Connect:** The browser uses the retrieved IP address to connect to the server.

## 5. How the Internet Works (Simplified)

The internet works by breaking down data into small packets and sending them across a vast network of interconnected devices (routers, switches, servers) using the **TCP/IP suite**.

1.  **Request (Client to Server):** When you click a link or type a URL, your device (the **Client**) creates a request (e.g., an HTTP GET request).
2.  **Packaging:** This request is broken down into small **packets**. Each packet is given a header containing the source IP, destination IP, and the order in which it should be reassembled.
3.  **Routing:** The packets travel from your device, through your router, through your ISP's network, and then across the internet's backbone infrastructure (fibers, cables).
    - **Routers** are key devices that examine the destination IP in the packet's header and use routing tables to determine the most efficient next path (hop) to the destination.
4.  **Assembly:** The packets eventually arrive at the destination server (the **Server**). The server reassembles the packets into the original request.
5.  **Response (Server to Client):** The server processes the request and sends a response (e.g., an HTML file) back to the client, following the same packet-based process, but with the source and destination IPs swapped.
6.  **Display:** Your browser reassembles the response packets and renders the webpage.

## 6. What is HTTP?

**HTTP (Hypertext Transfer Protocol)** is an application layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers (clients) and web servers.

- **Stateless:** Each command is executed independently, without any knowledge of the commands that came before it.
- **Client-Server Model:** It follows a request-response paradigm: a client sends a request, and a server returns a response.
- **Methods:** It defines methods (verbs) to indicate the desired action for the requested resource, such as **GET** (retrieve data), **POST** (submit data), **PUT** (update data), and **DELETE** (remove data).

## 7. The 7 Layers of the OSI Model

The **OSI (Open Systems Interconnection) Model** is a conceptual framework used to describe the functions of a networking system. It organizes communication into seven distinct layers, moving from the physical connection to the application the user interacts with.

| #     | Layer Name       | PDU (Protocol Data Unit) | Function/Description                                                                                     |
| :---- | :--------------- | :----------------------- | :------------------------------------------------------------------------------------------------------- |
| **7** | **Application**  | Data                     | Provides the interface for users and applications (HTTP, DNS, SMTP). **(HTTP Layer)**                    |
| **6** | **Presentation** | Data                     | Handles data formatting, encryption, and compression (JPEG, MP3).                                        |
| **5** | **Session**      | Data                     | Manages connections (sessions) between local and remote applications.                                    |
| **4** | **Transport**    | Segments                 | Handles end-to-end communication, segmentation, and reassembly (TCP, UDP).                               |
| **3** | **Network**      | Packets                  | Handles logical addressing (IP addresses) and routing of data (IP, ICMP).                                |
| **2** | **Data Link**    | Frames                   | Handles physical addressing (MAC addresses) and error control for the physical layer (Ethernet, Wi-Fi).  |
| **1** | **Physical**     | Bits                     | Defines the electrical, mechanical, and procedural specifications for the network medium (Cables, Hubs). |

### The HTTP Layer

**HTTP** is an **Application Layer (Layer 7)** protocol. It sits at the very top of the model, closest to the end-user. It relies on the services of the layers below it (like TCP/IP in the Transport and Network layers) to actually move the data across the network.

## 8. HTTP vs. HTTPS

The difference between HTTP and HTTPS is all about **security**.

| Feature         | **HTTP (Hypertext Transfer Protocol)**                    | **HTTPS (Hypertext Transfer Protocol Secure)**                                                   |
| :-------------- | :-------------------------------------------------------- | :----------------------------------------------------------------------------------------------- |
| **Security**    | **Insecure**. Data is transmitted in plain text.          | **Secure**. Data is encrypted before transmission.                                               |
| **Protocol**    | Application Layer Protocol.                               | HTTP with a secure layer (**SSL/TLS**).                                                          |
| **Port**        | Uses port **80** by default.                              | Uses port **443** by default.                                                                    |
| **Encryption**  | None.                                                     | Uses **SSL/TLS (Secure Sockets Layer/Transport Layer Security)** for encryption.                 |
| **Certificate** | Not required.                                             | Requires an **SSL/TLS Certificate** to verify the server's identity.                             |
| **Use Case**    | Rarely used today; only for non-sensitive public content. | **Standard for almost all websites**, especially those handling sensitive data (login, payment). |
