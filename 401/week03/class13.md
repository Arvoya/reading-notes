# Message Queues

## Questions and Answers

[Socket.io Chat Example](https://socket.io/get-started/chat/)

1. Explain to a non-technical recruiter what the Chat Example (above) does.
    So its basically a blueprint example for a simple chat application. It uses
    socket.io to send messages to everyone who is connected to ther server, by
    emitting html based on the message that is sent.
2. What proof of life are we getting on the backend from the above app?
    We are getting a console log that says "a user connected"
3. Socket.IO gives us the iO.emit() method to send an event to everyone. What flag
would you use if you want to send a message to everyone except for a certain emitting
socket?
    You would use the `broadcast` flag.

---

[Rooms](https://socket.io/docs/v4/rooms)

1. What is a room and how might a room be useful?
    Rooms are a way to gorup sockets together. This is useful for when you want to
    send a message to a specific group of people. Like a group chat!
2. How do you join a room?
    The `socket.join()` method is used to join a room. Followed by a string that
    is the name of the room.
3. How do you leave a room?
    The `socket.leave()` method is used to leave a room. Followed by a string that
    is the name of the room.

---

[Namespaces](https://socket.io/docs/v4/namespaces/)

1. What is a Namespace and what does it allow you to do?
    A Namespace is a communication channel that allows you to split the logic
    of your application over a single shared connection (also called "multiplexing").
2. Each namespace potentiallly has its own what? (hint: 3 things)
    - event handlers
    - rooms
    - middleware
3. Discuss a possible use case for separate namespaces
    Discord or slack would be a good example of using namespaces. You could have
    a namespace for each channel or room.

## Resources

[Socket.io Emit Cheatsheet](https://socket.io/docs/v4/emit-cheatsheet/)
