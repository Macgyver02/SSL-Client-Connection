# Simple SSL Client in C

This project is a simple SSL client implemented in C using the OpenSSL library. The client connects to a specified server using TLS/SSL, sends a message, and displays the server's response and certificate information.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [License](#license)

## Features

- Establishes a secure connection to a server using SSL/TLS.
- Sends a simple message ("Hello???") to the server.
- Receives and displays the server's response.
- Retrieves and prints the server's SSL certificates.

## Prerequisites

To compile and run this program, you will need:

- A C compiler (e.g., `gcc`)
- OpenSSL library installed on your system

On a Debian-based system, you can install OpenSSL with:

```sh
sudo apt-get install libssl-dev
```

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/ssl-client.git
    cd ssl-client
    ```

2. **Compile the code**:
    ```sh
    gcc -o ssl-client ssl-client.c -lssl -lcrypto
    ```

## Usage

To run the SSL client:

```sh
./ssl-client <hostname> <portnum>
```

- `<hostname>`: The server's hostname or IP address.
- `<portnum>`: The port number on which the server is listening.

For example:

```sh
./ssl-client example.com 443
```

This will connect to `example.com` on port `443` (the standard HTTPS port), send the message "Hello???", and print the server's response along with its SSL certificate details.

## Code Overview

- **`OpenConnection`**: Establishes a TCP connection to the specified hostname and port.
- **`InitCTX`**: Initializes the SSL context using the TLSv1.2 client method.
- **`ShowCerts`**: Retrieves and prints the server's SSL certificates.
- **`main`**: The main function that sets up the SSL connection, sends a message, and handles the server's response.

### Example Output

```sh
Connected with ECDHE-RSA-AES256-GCM-SHA384 encryption
Server certificates:
Subject: /C=US/ST=California/L=Mountain View/O=Google LLC/CN=*.google.com
Issuer: /C=US/O=Google Trust Services LLC/CN=GTS CA 1O1
Received: "HTTP/1.1 200 OK ..."
```

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
```

This `README.md` provides an overview of the project, installation instructions, usage examples, and a brief explanation of the code. Adjust the GitHub URL and other details as needed.
