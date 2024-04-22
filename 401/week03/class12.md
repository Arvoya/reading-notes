# Socket.io

## Questions and Answers

[Web Sockets](https://en.wikipedia.org/wiki/WebSocket)

1. What is a Web Socket?

    It is a computer communications protocol.

    ![A diagram describing a connection using WebSocket](https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Websocket_connection.png/220px-Websocket_connection.png)
    >Image from the wiki link above

2. Describe the Web Socket request/response handshake and what happens once the
connection is established.

    **Steps:**
    1. Opening handshake (HTTP request + HTTP response) to establish a connection
    2. Data messages to transfer application data
    3. Closing handshake (two Close frames) to close the connection

3. Web Sockets provide a standardized way for the server to send content to a client
without first receiving a ___ from that client.

    *requested*

---

[Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)

1. What does the event handler `io.on()` do?
    I listens for an event and then funs a callback function.
2. Describe some possible proof of life or proof that the code works as expected
    You can use the console.log to see if sockets are connected.
3. What does socket.emit() do?
    It sends a message to the main server.

---

[Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)

1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub,
or OAuth and AuthO).
The main difference is that WebSockets is a protocol and Socket.IO is a library.
2. When would you use Socket.IO?
When you are using javascript code and need to use websockets.
3. When would you use WebSockets?
When you want to have a server be able to update to multiple clients.

---

[Video - OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)

1. What are a couple of key takeaways from this video?
That there so much I don't know haha but the OSI model is behind the scenes of the
internet.

[Video - TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)

1. Translate the gist of this video to a non-technical friend
The video explains how transmission control protocol works from client to server.
There are various steps along the way to establish a connection, and lots of requiring
responses before moving to a following step.

## Other Resources

[Socket.io Documentation](https://socket.io/docs/)

[Socket.io Server API](https://socket.io/docs/server-api)

[Socket.io Client API](https://socket.io/docs/client-api)

[Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)

## Reflection

1. What are your learning goals after reading and reviewing the class [README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-12/)?

I'm really curious about making some sockets for messages. That seems like a really
neat thing to learn about.
