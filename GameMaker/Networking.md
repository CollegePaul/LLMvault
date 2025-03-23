### Networking in GameMaker

Networking in GameMaker allows developers to create multiplayer games that can be played over a network. This involves setting up a server-client architecture where one or more clients connect to a server to synchronize game state, send input data, and receive updates.

#### Server-Client Model:
- **Server**: The central hub that manages all connections, handles incoming requests, and distributes information to connected clients.
- **Clients**: The individual instances of the game that connect to the server, sending and receiving data based on user interactions and the server's updates.

### Key Functions:

1. **Network Creation**:
   - `network_create_server(port)`: Creates a server that listens for incoming connections on the specified port.
   - `network_connect_to_host(ip, port)`: Connects a client to a server at the given IP address and port number.

2. **Data Transmission**:
   - `network_send_packet(socket_id, buffer, len)`: Sends data from one instance to another over the network using a socket identifier.
   - `network_receive_packet(socket_id, buffer, maxlen)`: Receives data sent through a specific socket.

3. **Event Handling**:
   - Networking events like `Network Connect`, `Network Send`, and `Network Receive` are used in GameMaker Studio 2 to manage various network-related activities.

### Example: Simple Chat Application

Here's a basic example of how to set up a simple chat server-client application using GML:

#### Server Code:
```gml
// Create Event (Server)
network_create_server(6510);
show_debug_message("Server started on port 6510");

// Network Connect Event (Server)
var ip = argument0;
var port = argument1;
show_debug_message("Client connected: " + ip + ":" + port);

// Network Receive Event (Server)
var socket_id = argument0;
var buffer = ds_list_create();
network_receive_packet(socket_id, buffer, 64);
var message = buffer_read_string(buffer);
ds_list_destroy(buffer);
show_debug_message("Message received from client: " + message);

// Broadcast the message to all connected clients
var num_clients = network_get_connection_count();
for (var i = 0; i < num_clients; i++) {
    var client_socket_id = network_get_connection(i);
    buffer = ds_list_create();
    buffer_write_string(buffer, message);
    network_send_packet(client_socket_id, buffer, ds_list_size(buffer));
    ds_list_destroy(buffer);
}
```

#### Client Code:
```gml
// Create Event (Client)
network_connect_to_host("127.0.0.1", 6510);
show_debug_message("Connecting to server...");

// Network Connect Event (Client)
var ip = argument0;
var port = argument1;
show_debug_message("Connected to server: " + ip + ":" + port);

// Draw GUI Event (Client) - Simple input field
draw_rectangle(32, 32, 640, 96, false);
input_string_draw(40, 40, 592, 48, c_white);

// Network Receive Event (Client)
var socket_id = argument0;
var buffer = ds_list_create();
network_receive_packet(socket_id, buffer, 64);
var message = buffer_read_string(buffer);
ds_list_destroy(buffer);
show_debug_message("Message received from server: " + message);

// Step Event (Client) - Sending messages
if (keyboard_check_pressed(vk_return)) {
    var input_text = input_string_get_text();
    if (input_text != "") {
        buffer = ds_list_create();
        buffer_write_string(buffer, input_text);
        network_send_packet(network_get_connection(0), buffer, ds_list_size(buffer));
        ds_list_destroy(buffer);
        input_string_clear();
    }
}
```

This example demonstrates how to set up a basic server-client chat system. When the client sends a message, it is broadcasted to all connected clients by the server.

#Networking #GamaMaker