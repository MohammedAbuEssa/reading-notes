# Message Queues

### [Socket.io Chat Example](https://socket.io/get-started/chat/)

---

1. Explain to a non-technical recruiter what the Chat Example (above) does.  
   It shows you how to create a basic messaging app including backend and frontend.

2. What proof of life are we getting on the backend from the above app?

   "a user connected" & "listening on \*:3000"

3. Socket.IO gives us the i0.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?
   "broadcast.emit()"

---

### [Rooms](https://socket.io/docs/v4/rooms)

---

1. What is a room and how might a room be useful?

   A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

2. How do you join a room?

   You can call join to subscribe the socket to a given channel.

3. how do you leave a room?

   To leave a channel you call leave in the same fashion as join.

---

### [Namespaces](https://socket.io/docs/v4/namespaces/)

---

1. What is a Namespace and what does it allow you to do?

   A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection (also called "multiplexing").

2. Each namespace potentially has its own what? (hint: 3 things)

   - Event handlers
   - Rooms
   - Middlewares

3. Discuss a possible use case for separate namespaces

   - You want to create a special namespace that only authorized users have access to, so the logic related to those users is separated from the rest of the application.
   - Your application has multiple tenants so you want to dynamically create one namespace per tenant.

## [Main Page](../README.md)
