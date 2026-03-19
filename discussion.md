1. What is an IP address? (100 words) 
	* Why do we need IP addresses? 
	* What is the relation between TCP and IP? 
	* What is a socket? Have you heard of different types of sockets? 
	* What is up with the address: 127.0.0.1? 
	An IP address is the numeric value assigned to the device connected to a network.
	To differentiate between computers allowing us to communicate through the network. TCP allows reliable transfer of data between connections and IP transfers TCP packets connectionlessly not ensuring the packets delivered are complete.
	A socket is an endpoint between two programs running on a network allowing them to send and receive data. I have heard of a few sockets for example Stream sockets and Raw sockets. 
	127.0.0.1 is the loopback address so it will always return traffic to the same machine that created it.

2. What does a client-server architecture mean? (150 words) 
	* Give a concrete example of where you would encounter this in real life. 
	* How do you decide who is the server and who is the client? 
		Client server architecture is a method of designing software where the client and server interact with eachother requesting and sending data.
		We encounter this everywhere, all distributed systems are built on this concept however the specific software architecture varies and often combines many different patterns resulting in its own unique architecture. A concrete example is netflix or amazon which both heavily rely on cloud computing platforms. The client is the one interacting with the service while the server provides the resources, stores data, delivers the services etc.

3. What is the difference between client-server architecture and the broker architecture? (100 words) 
	* What are the benefits to the broker pattern? 
	* What could be potential downsides? 
		The broker architecture has a middleman which controls the flow of requests between the server and client i.e. the client and the server do not know of eachother, client server architecture is one on one between the client and server. The broker pattern is easier to scale and change as there is no dependency between the client and server. Since the broker generally controls all requests (depends on design) it can be devastating if someone manages to hack into the broker and thereby having full control to send requests to the client and server (basically it becomes a single point of complete failure and can affect the whole system).
        
4. What does Peer-to-Peer mean? (150 words) 
	* What are the main characteristics of this architecture? 
	* Have you encountered it anywhere online? 
	* Does Peer-to-Peer applications mean that there are no servers and only clients? 
	* What benefits could there be to using this pattern? 
	* What downsides could there be to this pattern?
		Peer to Peer architecture is a distributed network where clients relay data to eachother creating a net of interactions, the client also contributes as the server. It allows for quick data transfer when working with a large network however issues arise when the clients are few and unreliable since services can become unstable and or disappear fully. It exists all over the place for example torrents and blockchains. Peer to peer applications generally rely on the users for computations however there often exists a server to control the infrastructure of the platform. This pattern is extremely useful for file sharing and is used in bitcoin mining. Like mentioned the architecture can be unreliable when peers are unavailable and there are often security risks involved as the clients are relaying information.