


# **MultiRust**  
*A lightweight, multithreaded web server built in Rust.*

## **Overview**  
`MultiRust` is a minimal HTTP server built from scratch in Rust. It demonstrates the use of a custom thread pool to handle multiple client requests concurrently, efficiently managing resources and providing basic HTTP functionalities.

## **Features**  
- Handles multiple HTTP requests concurrently using a thread pool.  
- Routes requests to serve static files like `hello.html`.  
- Simulates long-running requests with a `/sleep` route.  
- Graceful shutdown after processing a limited number of requests.  
- Simple and extensible for further development.

## **Getting Started**

### **Prerequisites**
Ensure you have the following installed:
- Rust (latest stable version).  
You can install Rust via [rustup](https://www.rust-lang.org/tools/install).  

### **Installation**
1. Clone this repository:
   ```bash
   git clone https://github.com/Krishang91/multirust.git
   cd multirust
   ```
2. Build the project:
   ```bash
   cargo build --release
   ```

3. Run the server:
   ```bash
   cargo run
   ```

### **Usage**
1. Start the server.  
   By default, it binds to `127.0.0.1:7878`.  

2. Open your browser and navigate to:
   - [http://127.0.0.1:7878/](http://127.0.0.1:7878/) to get the content of `hello.html`.
   - [http://127.0.0.1:7878/sleep](http://127.0.0.1:7878/sleep) to simulate a long-running request.  

3. For unsupported routes, you’ll get a `404.html` response.

### **Example Request-Response**
#### Request:
```http
GET / HTTP/1.1
```
#### Response:
```http
HTTP/1.1 200 OK
Content-Length: 123

<!DOCTYPE html>
<html>
<head>
    <title>Hello</title>
</head>
<body>
    <h1>Welcome to MultiRust!</h1>
</body>
</html>
```

---

## **Customization**  
- Modify the `handle_connection` function to add more routes or serve dynamic content.  
- Extend the thread pool to handle dynamic resizing or better job prioritization.

---

## **Contributing**
Contributions are welcome! Feel free to fork the repository and submit a pull request with your changes.

---

## **License**
This project is licensed under the MIT License. See `LICENSE` for details.

---

## **Acknowledgments**
Inspired by "The Rust Programming Language" book's multithreaded web server example.

---
