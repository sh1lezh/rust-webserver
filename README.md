# Rust Webserver

A multi-threaded webserver built in Rust, following the example from *The Rust Programming Language* book. This project demonstrates handling HTTP requests concurrently using a thread pool and Rust's standard library.

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Features
- Handles HTTP GET requests concurrently using a thread pool
- Serves static HTML content
- Responds with HTTP status codes (e.g., 200 OK, 404 Not Found)
- Built with Rust's standard library (`std::net`, `std::io`, `std::thread`)

## Prerequisites
To run this webserver, you need:
- [Rust](https://www.rust-lang.org/tools/install) (stable version recommended)
- A terminal or command-line interface
- Basic knowledge of HTTP and Rust

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/sh1lezh/rust-webserver.git
   cd rust-webserver
   ```
2. Ensure Rust is installed. Verify with:
   ```bash
   rustc --version
   ```
   If Rust is not installed, follow the [official Rust installation guide](https://www.rust-lang.org/tools/install).
3. Build the project:
   ```bash
   cargo build --release
   ```

## Usage
1. Run the webserver:
   ```bash
   cargo run
   ```
   The server will start and listen on `127.0.0.1:7878` by default, handling requests concurrently with a thread pool.
2. Open a web browser and navigate to:
   ```
   http://localhost:7878
   ```
   - Visiting `/` will serve a `hello.html` page (if available in the project directory).
   - Visiting `/sleep` will simulate a delayed response (if implemented).
   - Any other route will return a 404 error with a `404.html` page.
3. To stop the server, press `Ctrl+C` in the terminal.

## Project Structure
```
rust-webserver/
├── src/
│   └── main.rs       # Main server logic with thread pool implementation
├── hello.html        # Static HTML file for the root endpoint
├── 404.html          # Static HTML file for 404 responses
├── Cargo.toml        # Rust project configuration
└── README.md         # This file
```

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

Please ensure your code follows Rust's coding conventions (use `cargo fmt`) and includes appropriate tests.
