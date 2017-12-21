# NetworksAssignments

- Assignment (1)
  - using sockets programming in c++, Simple Http clinet/server are implemented. 
  - ServerAlgorithm  
    - Listen for connections
    - Accept new connection from incoming client and delegate it to worker thread/process
    - Parse HTTP/1.0 request and determine the command (GET or POST)
    - Determine if target file exists (in case of GET) and return error otherwise
    - Transmit contents of file (reads from the file and writes on the socket) (in case of GET)
  - ClientAlgorithm 
    - Create a TCP connection with the server
    - Wait for permission from the server
    - Send next requests to the server
    - Receives data from the server (in case of GET) or sends data (in case of POST)
- Assignment (2)
  - Two Algorithms are implemented selective repeat, and stop and wait for the server 
    that guarantees reliable data transfer along with congestion control handling.   
  - StopAndWait: The server sends a single datagram, and blocks until an acknowledgement from the client is
    received or timeout.
  - SelectiveRepeat: The server is allowed to have up to N datagrams that have not yet been
    acknowledged by the client. 
  
- Assignment (3)
  - using ns-3-27 [https://www.nsnam.org/ns-3-27/] to simulate Open Shortest Path First (OSPF) algorithm. 
  - OSPF is a link state routing protocol, implemented in each router. 
  - A script first.c is created to simulate a topology with six nodes (one for the server and the others are clients), 
    with those nodes having point to points links, and internet stack installed.
  - the GlobalRouting implementation in NS3 keeps all routes to the node in the database, it's updated to keep only 
    the route with the min number of hops (least cost).   
