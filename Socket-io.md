...
What is a Web Socket?
   A WebSocket is a communication protocol that provides full-duplex communication channels over a single TCP (Transmission Control Protocol) connection. It enables real-time, bidirectional communication between a client and a server.

   In traditional web communication, the client (typically a web browser) sends an HTTP request to the server, and the server responds with the requested data. However, this communication model is based on a request-response paradigm, where the server cannot initiate communication with the client unless the client sends a new request.

   WebSockets, on the other hand, establish a persistent connection between the client and the server, allowing both parties to send data to each other at any time without the need for explicit requests. This enables real-time and interactive communication between the client and the server.


Describe the Web Socket request/response handshake and what happens once the connection is established.
   - Client sends an HTTP request: The client initiates the WebSocket connection by sending an HTTP request to the server. This request includes the special Upgrade header with a value of websocket, indicating that the client wants to establish a WebSocket connection.

   - Server responds with an HTTP response: Upon receiving the client's request, the server evaluates it. If the server supports WebSocket connections and accepts the upgrade request, it responds with an HTTP response. This response includes a status code of 101 Switching Protocols and the Upgrade header set to websocket.

   - Connection is upgraded to WebSocket: Once the server's response is received, the client and server upgrade the connection from HTTP to the WebSocket protocol. This transition includes switching from the HTTP-based communication model to the WebSocket-based communication model.

   - WebSocket connection is established: With the connection upgraded, the WebSocket connection is now established between the client and the server. Both parties can now exchange messages and data over the WebSocket connection.

   - Bidirectional communication begins: Once the WebSocket connection is established, both the client and the server can send messages to each other without the need for explicit requests. They can send data in both directions simultaneously, enabling real-time bidirectional communication.

   - Continuous connection: The WebSocket connection remains open until either the client or the server explicitly closes it. This allows for continuous and persistent communication between the client and the server.

   - Data transfer: After the connection is established, the client and server can exchange data using the WebSocket protocol. Each message is wrapped in a WebSocket frame and can be sent and received by either party.

   - Closing the connection: Either the client or the server can send a WebSocket close frame to initiate the closure of the connection. Once the close frame is received by the other party, they respond with a close frame, and the connection is closed gracefully.


Web Sockets provide a standardized way for the server to send content to a client without first receiving a request (message) from that client.

What does the event handler io.on() do?

   - io represents the instance of the socket.io server that you have created. It is typically set up using const io = require('socket.io')(server), where server is the HTTP server object.

   - io.on(event, callback) is used to register an event handler for a specific event on the server side. The event parameter specifies the event name you want to listen for, and the callback parameter is the function that will be executed when that event is triggered.

   - When a client emits an event with the specified name, the server receives that event and invokes the callback function associated with it.

WebSocket is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer. When clients trigger the request to the server, it does not close the connection on receiving the response; it rather persists and waits for the Client or server to terminate the request.

Socket.IO is a library that enables real-time and full-duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts; both WebSocket vs Socket.io are event-driven libraries.