
# Week 1: Internet and Web Fundamentals

## Learning Objectives

- **Understand the Client-Server Model:** Learn how a browser (client) requests resources and a server responds.  
- **Explain HTTP/HTTPS protocols:** Learn how web requests are made (GET, POST, etc.), what status codes (200, 404, 500) mean, and why HTTPS secures data.  
- **Describe DNS:** Learn how human-friendly domains (e.g., `google.com`) are translated into IP addresses.  
- **Define Web Servers:** Understand server software (like Apache, Nginx, or a Node.js app) that stores and serves HTML/CSS/JS content.  
- **Outline the Browser Rendering Process:** Learn how a browser parses HTML, CSS, and JavaScript, builds the DOM/CSSOM, and paints the page.  

---

## Topic Summaries

### Client-Server Model

- The Internet is built on a **client-server pattern**: the client (e.g., your web browser) asks for data and the server (a remote computer) provides it.  
- For example, entering a URL causes the browser to send a request to a web server, and the server returns the requested webpage.

### HTTP/HTTPS Protocols

- **HTTP (HyperText Transfer Protocol):** The protocol for web communication between browsers and servers.  
- **Methods:** Common request methods include `GET` (retrieve data) and `POST` (send data).  
- **Status Codes:** Servers reply with codes like `200 OK` (success), `404 Not Found` (resource missing), or `500 Internal Server Error` (server problem).  
- **HTTPS:** HTTP with encryption (TLS/SSL) to secure data in transit.

### DNS (Domain Name System)

- **DNS:** Acts like the Internet’s phonebook, translating human-friendly domain names (e.g. `www.example.com`) into IP addresses (e.g. `192.0.2.1`).  
- **Process:** When you type a website name, your computer queries a DNS server to get the server’s numeric IP address so browsers can find each other.

### Web Servers

- **Web Server:** Software (running on a server computer) that listens for HTTP requests and sends back web content (HTML pages, images, scripts).  
- **Examples:** Apache (open-source HTTP server) and Nginx (high-performance server/reverse-proxy) are popular.  
- **Node.js:** Using its built-in HTTP module, a Node.js program can also act as a simple web server to serve files or API responses.

### Browser Rendering Process

- **Parsing:** Browser parses HTML into the DOM (Document Object Model) and CSS into the CSSOM.  
- **Render Tree:** DOM and CSSOM are combined into a render tree containing only visible elements.  
- **Layout (Reflow):** The browser computes the size and position of each element in the render tree.  
- **Painting:** The browser paints the pixels on screen for each element (text, colors, borders, images).  
- **JavaScript:** Scripts are parsed and executed by the JS engine; they can modify the DOM/CSSOM, causing re-layout and repaint.

---

## Beginner-Friendly Explanations

### Client-Server Model

In the client-server model, the **client** (browser/app) asks for something, and the **server** provides it.  
For example, typing `www.example.com` in a browser causes the browser to:

1. Perform a **DNS lookup** to find the server’s IP.
2. Send an **HTTP GET** request to the server.
3. Receive the HTML, CSS, JS, and images.
4. Render the page.

Analogy: Like ordering pizza — you (the client) call the pizza shop (the server), they make and deliver it.

### HTTP/HTTPS Protocols

- `GET`: Request data  
- `POST`: Send data to create/update  
- `PUT`: Create or update  
- `DELETE`: Remove a resource  

**Status Codes:**

- `200 OK`: Success  
- `404 Not Found`: Resource doesn't exist  
- `500 Internal Server Error`: Server crashed  

**HTTPS**: HTTP + encryption. Secures data via TLS/SSL. Look for the 🔒 padlock in your browser.

### DNS

- Converts names (`google.com`) → numbers (`142.250.190.14`)  
- Like a phonebook: names = people, IPs = phone numbers  
- Without DNS, we'd have to memorize IPs  
- Flow: `domain → DNS lookup → IP → HTTP request → content`

### Web Servers

- Wait for browser requests → serve HTML/CSS/JS/images  
- **Apache** and **Nginx** = popular servers  
- **Node.js** can act as a server via built-in HTTP module  
- Servers read files and respond over HTTP

### Browser Rendering Process

Steps:
1. Parse HTML → DOM
2. Parse CSS → CSSOM
3. Merge → Render Tree
4. Layout → calculate sizes & positions
5. Paint → draw on screen  
6. JavaScript runs and can modify DOM/CSSOM (repaint/reflow)

---

## Illustrative Examples or Diagrams

### Client-Server Diagram
> Clients send HTTP requests to the server. The server processes the requests and returns responses.

### DNS & HTTP Request Flow
> Browser requests a domain → DNS resolves to IP → Browser sends GET to IP → Server returns page.


---

## Suggested Activities or Exercises

- **Client-Server Inspection:** Open browser dev tools → Network tab → Reload a page → Observe HTTP methods & status codes.  
- **HTTP Testing:** Use Postman or `curl` to send GET/POST/invalid requests.  
- **DNS Practice:** Use `nslookup google.com` or `dig` to view IP address.  
- **Local Server:**  
  ```bash
  python3 -m http.server
  ```  
  Open `http://localhost:8000` in a browser and test changes in `index.html`.

- **DOM Exploration:** Right-click a webpage → Inspect → Edit HTML/CSS → Watch real-time changes.

---

## Key Takeaways

- The **client-server model** is the foundation of the web: browsers (clients) request resources and servers provide them.  
- **HTTP** is the protocol for web communication. Clients use methods like GET/POST to request data, and servers respond with status codes (e.g. 200 OK for success, 404 Not Found if a page is missing, 500 Internal Server Error for server failures).  
- **HTTPS** adds encryption (TLS/SSL) to HTTP, securing data between browser and server (look for the padlock icon in the address bar on secure sites).  
- **DNS** acts like a phonebook, mapping human-friendly domain names to numeric IP addresses (e.g. `example.com` → `93.184.216.34`). This lets us use easy names instead of remembering hard-to-remember IPs.  
- A **web server** is software that listens for HTTP requests and serves files (HTML/CSS/JS). Examples include Apache and Nginx (dedicated servers) or a custom server built with Node.js. Web servers make websites accessible over the Internet.  
- The **browser rendering process** converts code into what you see on screen: HTML is parsed into the DOM, CSS into the CSSOM, which combine into a render tree. The browser then computes layout (sizes/positions) and paints pixels. JavaScript is parsed/executed during this process and can dynamically update the page.  
