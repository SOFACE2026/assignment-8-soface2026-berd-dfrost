1. What is an IP address? (100 words) 
    * Why do we need IP addresses? 
    * What is the relation between TCP and IP? 
    * What is a socket? Have you heard of different types of sockets? 
    * What is up with the address: 127.0.0.1? 
    An IP address is the numeric value assigned to the device connected to a network, to differentiate between computers, allowing us to communicate through the network.
    TCP allows reliable transfer of data between connections. IP allows transfers of packets, and TCP is a protocol for ensuring robust transfer of those packets, such as the correct ordering and retransmission of lost packages. 
    A socket is the combination of an IP and a Port. It serves as an endpoint between two programs running on a network. I have heard of a few sockets, for example Stream sockets(TCP), Datagram sockets(UDP), and Raw sockets. 
    127.0.0.1 is the loopback address so it will always return traffic to the same machine that created it.

2. What does a client-server architecture mean? (150 words) 
    * Give a concrete example of where you would encounter this in real life. 
    * How do you decide who is the server and who is the client? 
        Client server architecture is a method of designing software where the client and server interact with eachother via requests and replies.
        We encounter this everywhere, all distributed systems are built on this concept, however the specific software architecture varies, and often combines many different patterns, resulting in its own unique architecture. A concrete example is Netflix or Amazon, which both heavily rely on cloud computing platforms. The client is the one interacting with the service while the server provides the resources, stores data, delivers the services etc. Very generally, the server provides a service, and the client makes use of that service. An example of this architecture a single system, instead of a distributed system, is the operating system, which has servers that provide much of the core functionality.

3. What is the difference between client-server architecture and the broker architecture? (100 words) 
    * What are the benefits to the broker pattern? 
    * What could be potential downsides? 
        The broker architecture has a middleman, which controls the flow of requests between the server and client i.e. the client and the server do not know of eachother. Client-server architecture is instead one on one between the client and server. The broker pattern is easier to scale and change as there is no dependency between the client and server. Since the broker generally controls all requests(depends on design), it can be devastating if it fails, or if someone manages to hack into the broker. Basically, it becomes a single point of failure.
        
4. What does Peer-to-Peer mean? (150 words) 
    * What are the main characteristics of this architecture? 
    * Have you encountered it anywhere online? 
    * Does Peer-to-Peer applications mean that there are no servers and only clients? 
    * What benefits could there be to using this pattern? 
    * What downsides could there be to this pattern?
        Peer to Peer architecture is a distributed network where clients relay data to eachother creating a net of interactions, where a client also contributes as a server. It allows for quick data transfer when working with a large network, and very low or even no overhead for a service provider. Issues arise however when the clients are few and unreliable, since services can become unstable or fail. Servers are sometimes involved for discovery and linking peers, either to make new connections, or to make redundant connections that boost robustness for when one or more peers drop out.
        It exists all over the place, for example torrenting, blockchains, and in online video games. This pattern is extremely useful for file sharing and is used in bitcoin mining. For video games it's useful because it removes the need for an expensive centralized server to maintain the connection. Like mentioned, the architecture can be unreliable when peers are unavailable and there are often security risks involved as the clients are directly interrelaying information.
