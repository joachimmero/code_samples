Winsock-server + Unity plugin

Introduction:

This project is a non-authoritative server written in C++ using the winsock2-library and a plugin for
Unity written in C#, which is used to connect to the server and use it.

Server-functionality:

1. Listens for client connections, accepts them and sends the client to a "hub".
2. In the hub, the server listens if the client wants to create a room or join an already existing one.
After getting the request, the server creates the room or adds the client to a room.

3. In the room, the server listens for byte-arrays sent from the client, and sends the array to every
client that is connected to the same room.

4. If a client leaves the room, the server informs the other clients that a client has left. 					