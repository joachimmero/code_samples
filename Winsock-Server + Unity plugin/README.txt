Winsock-server + Unity plugin

Introduction:

This project is a non-authoritative server written in C++ using the winsock2-library and a plugin for
Unity written in C#, which is used to connect to the server and use it.

Server-functionality:

1. The server listens for client connections and accepts them.

2. The server moves the client to a "hub", where it listens if the client wants to create or
join a room.	

3. Depending on the request, the server creates a room or adds the client to an already existing one.

4. In the room the server listens for byte-arrays from the client and sends the array to all other
clients connected to the room.

5. If a client leaves the room, the server informs all other clients connected to the room, that a client
has disconnected.

Unity-plugin-functionalities:

Formatter

	Handles the serialization and de-serialization of packages and methods that sent and received.

HalkoAttributeHandler

	Holds a method for getting a list of all methods that are marked with a certaing attribute.

HalkoClientHandler

	Handles the instantiation of new clients that connected the room and deletion of clients that left the room.

HalkoMethod

	Holds the "HalkoMethod" -attribute, that can be used to mark serializable methods.

	Holds the "HalkoClass" -class, that is a parent class, which is used to mark classes that hold "HalkoMethods".
	The "HalkoClass" -class also has methods for getting a list of HalkoMethods in it's child class and 
	invoking HalkoMethods on remote clients (sending the method through the server) and local clients.

HalkoMethodHandler

	Handles invoking the HalkoMethods, that are received from other clients.


HalkoNetwork
		
	Holds methods for connecting to the server, creating a room, joining a room, leaving a room, 
	getting the player count of a room, getting the room count of the server.

	Holds the callbacks for the methods listed above.

	Handles receiving data from the server and distributing it correctly.

HalkoPlayer

	A network "transform" -class. It handles moving and rotating player-objects locally and sending the 
	transform data through the server to other clients.

Package

	A struct that holds a player-objects position- and rotation-data.

Room

	A class that holds the information of a single room.

