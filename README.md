# HTTP Protocol Implementation in C++

## Overview
This project implements HTTP protocol as a C++ wrapper over C socket library. The implementation is a modular design with separate libraries for networking, utilities, and HTTP-specific functionality. It provides an HTTP server and client built over a socket-based communication system, enabling efficient request handling and response generation.

## Features
- **Custom Socket Implementation**: Includes an IPv4-based socket communication layer.
- **Multithreaded Server**: Handles concurrent HTTP requests efficiently.
- **HTTP Request and Response Handling**: Supports basic request parsing and response generation.
- **WebSockets Integration**: Enables persistent, low-latency bidirectional communication between clients and servers.
- **Exception Handling**: Ensures robustness with custom exception classes.
- **Real-Time Communication**: Conceptually aligned with Kafka for event streaming and MQTT for low-latency messaging.

## Project Structure
```
http_protocol_cpp/
│── include/net/        # Header files
│── net_socket/         # Networking library (socket implementation)
│── http/               # HTTP-specific components
│── util/               # Utility functions
│── CMakeLists.txt      # Build configuration
```

## Build Instructions
### Prerequisites
- C++ Compiler (GCC/Clang/MSVC)
- CMake (version 3.23 or later)

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/dikshamehta/HTTP-Protocol-Implementation
   ```
2. Create a build directory and configure the project:
   ```sh
   mkdir build && cd build
   cmake ..
   ```
3. Compile the project:
   ```sh
   make
   ```

## Libraries
The project is divided into the following libraries:
- **`util`**: General-purpose utilities.
- **`net_socket`**: Abstraction over sockets, providing network communication features.
- **`http`**: Implements HTTP request/response handling, HTTP server, and HTTP client.

[//]: # (## Usage)

[//]: # (### Running the HTTP Server)

[//]: # (After building the project, you can run the server as follows:)

[//]: # (```sh)

[//]: # (./http_server)

[//]: # (```)

[//]: # ()
[//]: # (### Running the HTTP Client)

[//]: # (```sh)

[//]: # (./http_client <server-address> <port>)

[//]: # (```)

## Using in Another Project
To use this project in another CMake-based project, add the following lines to your `CMakeLists.txt`:
```cmake
FetchContent_Declare(
        http
        GIT_REPOSITORY https://github.com/dikshamehta/HTTP-Protocol-Implementation.git
)
FetchContent_MakeAvailable(http)
```

## Future Improvements
- Support for HTTPS
- More HTTP methods (PUT, DELETE, etc.)
- Improved logging and debugging utilities
