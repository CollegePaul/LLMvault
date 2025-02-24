### Socket Programming in C++

Socket programming provides a mechanism to enable network communications between various devices over a network, such as the Internet. It allows different applications running on different platforms to communicate with each other. In C++, socket programming involves using system calls provided by the operating system to create and manage sockets.

Here’s a brief overview of key components in socket programming:

1. **Creating a Socket:** This is done using the `socket()` function, which returns a socket descriptor.
2. **Binding a Socket:** The `bind()` function associates the socket with a specific address and port number on the machine.
3. **Listening for Connections:** For server sockets, the `listen()` function allows the process to listen on the socket for incoming connections.
4. **Accepting Connections:** When a client connects to the server, the server calls `accept()`, which returns a new socket descriptor representing the connection.
5. **Reading and Writing Data:** The `read()` and `write()` functions are used to send and receive data over the socket.
6. **Closing Sockets:** Once communication is complete, sockets should be closed using the `close()` function.

### Example in C++

Here’s a simple example of a server-client program using sockets in C++:

#### Server Code
```cpp
#include <iostream>
#include <cstring>
#include <unistd.h>
#include <arpa/inet.h>

int main() {
    int server_fd, new_socket;
    struct sockaddr_in address;
    int addrlen = sizeof(address);
    char buffer[1024] = {0};
    const char* hello = "Hello from server";

    // Creating socket file descriptor
    if ((server_fd = socket(AF_INET, SOCK_STREAM, 0)) == 0) {
        perror("socket failed");
        exit(EXIT_FAILURE);
    }

    address.sin_family = AF_INET;
    address.sin_addr.s_addr = INADDR_ANY;
    address.sin_port = htons(8080);

    // Bind the socket to the port
    if (bind(server_fd, (struct sockaddr *)&address, sizeof(address)) < 0) {
        perror("bind failed");
        close(server_fd);
        exit(EXIT_FAILURE);
    }

    // Listen for connections
    if (listen(server_fd, 3) < 0) {
        perror("listen");
        close(server_fd);
        exit(EXIT_FAILURE);
    }

    // Accept a connection
    if ((new_socket = accept(server_fd, (struct sockaddr *)&address, (socklen_t*)&addrlen))<0) {
        perror("accept");
        close(server_fd);
        exit(EXIT_FAILURE);
    }

    // Read from the socket
    read(new_socket, buffer, 1024);
    std::cout << "Received: " << buffer << std::endl;

    // Send a response
    send(new_socket, hello, strlen(hello), 0);
    std::cout << "Hello message sent" << std::endl;

    // Close the sockets
    close(new_socket);
    close(server_fd);

    return 0;
}
```

#### Client Code
```cpp
#include <iostream>
#include <cstring>
#include <unistd.h>
#include <arpa/inet.h>

int main() {
    struct sockaddr_in serv_addr;
    int sock = 0, valread;
    char buffer[1024] = {0};
    const char* hello = "Hello from client";

    if ((sock = socket(AF_INET, SOCK_STREAM, 0)) < 0) {
        std::cout << "\n Socket creation error \n";
        return -1;
    }

    serv_addr.sin_family = AF_INET;
    serv_addr.sin_port = htons(8080);

    // Convert IPv4 and IPv6 addresses from text to binary form
    if(inet_pton(AF_INET, "127.0.0.1", &serv_addr.sin_addr) <= 0) {
        std::cout << "\nInvalid address/ Address not supported \n";
        return -1;
    }

    // Connect to the server
    if (connect(sock, (struct sockaddr *)&serv_addr, sizeof(serv_addr)) < 0) {
        std::cout << "\nConnection Failed \n";
        return -1;
    }

    send(sock, hello, strlen(hello), 0);
    std::cout << "Hello message sent\n";

    valread = read(sock, buffer, 1024);
    std::cout << "Received: " << buffer << std::endl;

    // Close the socket
    close(sock);

    return 0;
}
```

### Example in Python

Here’s a simple example of a server-client program using sockets in Python:

#### Server Code
```python
import socket

server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
host = '127.0.0.1'
port = 8080

server_socket.bind((host, port))
server_socket.listen(3)

print("Server listening on {}:{}".format(host, port))

client_socket, addr = server_socket.accept()
print("Connected to:", addr)

data = client_socket.recv(1024).decode('utf-8')
print("Received from client:", data)

message = "Hello from server"
client_socket.send(message.encode('utf-8'))

client_socket.close()
server_socket.close()
```

#### Client Code
```python
import socket

client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
host = '127.0.0.1'
port = 8080

client_socket.connect((host, port))

message = "Hello from client"
client_socket.send(message.encode('utf-8'))

data = client_socket.recv(1024).decode('utf-8')
print("Received from server:", data)

client_socket.close()
```

#Socket Programming #cpp