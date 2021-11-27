# 04 - Network Protocols

- What is a protocol?
    - Set of rules for an interaction between two parties.
    - For example a communication protocol.
- For networking, a communication protocol is going to be between to machines.
- Network protocol:
    - Kinds of messages sent and received (client/server).
    - The format of those messages.
    - The order of those messages.
    - Details on if there should be a response to that message.
        - What that response should look like.
    - Rules on when messages can be sent to one another.
- A lot of network protocols out there.
- There are a few that are very popular and important to know.
- IP, TCP & HTTP.
- IP:
    - Internet protocol.
    - IP address.
    - The modern internet effectively runs/operates on the IP.
    - When two machines communicate with each other over the internet, the data is transmitted in what are called IP packets.
    - IP packet:
        - The fundamental unit of data that is sent from one machine to another over the internet.
        - Made up of bytes.
        - Two main sections:
            - IP header:
                - At the beginning.
                - Contains useful info about the packet:
                    - Source IP of the packet.
                    - Destination IP of the packet.
                    - Total size of the packet.
                    - Version of the IP that this packet is operating by.
                        - Two versions in practice:
                            - Version 4: IPV4.
                            - Version 6: IPV6.
                - 20 - 60 bytes.
            - Data:
                - Contains the actual info that is being sent.
                - Limited in size: 2^16 bytes (about 65,000 bytes).
        - Usually multiple packets are sent.
        - Complicated: IP: Don't have a way of guaranteeing that these packets are going to be received.
        - Might get "lost".
        - Not guaranteeing the order these packets are read.
        - IP protocol alone, falls apart here.
        - This is where TCP comes into place.
- TCP:
    - Transmission control protocol.
    - Build on top of the IP.
    - Meant to solve the issues mentioned above.
    - Meant to send IP packets:
        - In an ordered way.
        - Reliable way.
            - Else know if particular packets repeatedly fail to be received.
        - Error free way.
            - Corrupted? Resend.
    - Used in virtually all web applications.
    - Allows you to send arbitrary long pieces of data.
    - Sits in the data portion of the IP packet.
    - Header (In the data portion of the IP packet):
        - Info about the ordering of packets.
    - When a machine whats to communicate with another machine:
        - Needs to set up a TCP connection.
        - Happens via a handshake:
            - Special TCP interaction.
    - Connection can be timed out.
    - Machines can end the connection.
    - Lacks:
        - Robust framework that developers can use to really define meaningful and easy to use communication channels for machines in a system.
        - It's only arbitrary data.
- HTTP:
    - Hypertext transfer protocol.
    - Built on top of TCP.
    - Introduces:
        - Higher lever abstraction above TCP.
        - Request & response paradigm.
            - With a set of accompanying rules.
    - Developers can use this to build robust and easy to maintain systems.
    - Most modern day systems rely on the HTTP protocol for communication.
    - Requests have a lot of properties that are defined by the HTTP protocol:
        - Host. 
        - Port.
        - Method (GET, POST, PUT, DELETE, etc.):
            - Describe the purpose of the request.
            - These are guidelines. You can use as you want.
        - Path.
            - Where you have logic in your server.
        - Headers.
            - Key-value. Metadata.
            - A lot of headers.
        - Body.
        - Etc.
        - A particular method and path can be configured to be an "endpoint" in the code.
    - Responses:
        - Status code.
        - Headers.
        - Body.
        - Etc.
- IP and TCP: For the transportation of data.
- HTTP: Introduces the opportunity to add a lot of business logic.