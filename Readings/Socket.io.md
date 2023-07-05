# Socket.io

### [Web Sockets](https://en.wikipedia.org/wiki/WebSocket)

1. What is a Web Socket?

 WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. The WebSocket protocol was standardized by the IETF as RFC 6455 in 2011. The current API specification allowing web applications to use this protocol is known as WebSockets. It is a living standard maintained by the WHATWG and a successor to The WebSocket API from the W3C.

2. Describe the Web Socket request/response handshake and what happens once the connection is established.

 The WebSocket request/response handshake is an initial process where the client and server exchange special HTTP headers to establish a WebSocket connection. Once the connection is established, it allows for real-time, bidirectional communication between the client and server without the need for repeated requests. WebSocket offers lower overhead, faster data transfer, and is compatible with existing infrastructure and web browsers.

3. Web Sockets provide a standardized way for the server to send content to a client without first receiving a requested from that client.


---

### [Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)

1. What does the event handler io.on() do?

The io.on() method is used to define event handlers for various events that can occur on the server side.

2. Describe some possible proof of life or proof that the code works as expected



3. What does socket.emit() do?

In Socket.IO, the socket.emit() function is used to send a custom event or message from the server to the client (or from one client to another client).

---

### [Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)

1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).

WebSocket is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer. When clients trigger the request to the server, it does not close the connection on receiving the response; it rather persists and waits for the Client or server to terminate the request.

Socket.IO is a library that enables real-time and full-duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts; both WebSocket vs Socket.io are event-driven libraries.

2. When would you use Socket.IO?

a). Real-time Web Applications: Socket.IO is commonly used for building real-time web applications that require instant updates and bidirectional communication between the server and clients. It provides a higher-level API and additional features like automatic reconnection, event-based communication, and room management, making it easier to develop real-time applications.

b). Cross-Browser Support: Socket.IO is designed to work across different browsers and provides fallback mechanisms such as long polling or AJAX-based communication when WebSocket support is not available. This makes it a suitable choice for applications that need to support a wide range of browser environments.

c). Scalability and Load Balancing: Socket.IO supports horizontal scalability and load balancing out of the box. It provides features like sticky sessions and the ability to distribute incoming connections across multiple servers, making it suitable for applications that require high scalability and handle a large number of concurrent connections.


3. When would you use WebSockets?

a). Low-Latency and Real-time Communication: WebSockets offer a lower level, lightweight, and efficient protocol for real-time communication. They are ideal for applications where low-latency, instant data transfer, and real-time updates are crucial, such as chat applications, real-time monitoring systems, live sports scores, or financial tickers.

b). High-Performance Applications: WebSockets provide a direct, persistent connection between the client and server, eliminating the need for continuous HTTP polling or long-polling techniques. This results in reduced overhead, improved performance, and better utilization of server resources.

c) Standardized WebSocket Protocol: If you have specific requirements that demand adherence to the WebSocket protocol standards, or you need to integrate with existing WebSocket-based systems or infrastructure, using plain WebSockets may be a better choice.

In summary, Socket.IO is suitable for building real-time web applications that require cross-browser support, high-level abstractions, and scalability, while WebSockets are ideal for low-latency, high-performance applications where adherence to WebSocket protocol standards or integration with existing WebSocket infrastructure is important.


---

### [OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0&ab_channel=TechTerms)

What are a couple of key takeaways from this video?

---

### [TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk&ab_channel=SunnyClassroom)

Translate the gist of this video to a non-technical friend

## [Main Page](../README.md)
