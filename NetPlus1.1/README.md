Hello there! These are additional Notes through Professor Messor. I am hoping to make these all short and sweet. They will all also be tagged with there 
corrisponding place on the Network+ N10-008 CompTIA Exam Objectives. Enjoy.

PDU (Protocol Data Unit)

Transmission units
    - A different group of data at different OSI layers.
We are taking a little bit of data and transmitting it across the network as a SINGLE UNIT.
EX: We know that layer 2 or the Data link layer is going to encapsulate the data to insure the data moves from One MAC address
to the Next MAC address.
DOESN'T care whats on the inside of the Frame.

The next layer IP operates on a Packet of Data
- Inside is TCP or UDP or something else, but it doesn't really care. It's Job is to take the data from end point to end point.
Or said another way, from one IP address to another.

The next layer is going to have one of two things. 
A TCP SEGMENT || a UDP DATAGRAM  with in this part of the packet.

Step through:
 Pretend we open a browser and we want to send data from the Web Server to the Web Client

Layers 5,6,7:  Application Data

Layer 4: | TCP |  | Application|       So we put a TCP Header in front of the Application Data
Transport  | Header| | Data  |
Layer







Layer 3:  | IP  |  | TCP  | | Application |  We need IP address to send the TCP data so we must add an IP Header to move

Network   | Header| | Header|  | Data     |  data from one IP address to Another IP address
Layer




Layer 2 :  |Frame|  | IP  |  | Application  | | Frame  |   Over Ethernet we need to have a DLC or Data Link Control layer 2 fram header and  
Data Link      |Header|   | Header|  |Data   |  | Trailer|  frame trailer to indicate the start and where the end of this frame might be.
Layer            




Order of opperations:
Sending...
Data Starts at Layer 7 and goes down to 1            Data appears at layer 7 in human readable format. (Applications: HTTPS, IMAP, SSH, etc)
Layer 6                                              Layer 6
Layer 5                                              Layer 5        
Layer 4   TCP/UDP                                    Layer 4  TCP/UDP
Layer 3   IP                                         Layer 3  IP
Layer 2   MAC                                        Layer 2  MAC 
---> >------ Binary data -------> > >  ------------  Data is received and moves up to 7


TCP Flags

The header describes or identifies the payload
- Here's what you're about to see...
The control information is setting bits in the header of each packet 
Each bit has a particular definition


This means that the device receiving this dat can interpret those bits and inderstand how to process the data properly. 
These bits are called "Control Flags" 

The TCP header contains important control information
- Includes a set of bits called TCP flags

How do flags work?

The header describes or identifies the payload
-   Here's what you're about to see...
The TCP header contains important control information
- Includes a set of bits called TCP flags
The flags control the payload
    - SYN: Synchronize sequence numbers
    -PSH: Pushes the data to the application w/out buffering
    -RST: Reset the connection
    -FIN: Last packet from the sender
By turning on/off these different flags we can change how a device may interpret the rest of the data
being sent using the tcp header.


There are also FLAGS w/in IP headers. Most of the FLAGS w/in the IP header deal 
with the fragmentation of data.
EX: there may be a times where you want to send traffic across the network but because of the 
architecture or design of the network your not able to send packets that are very large.

In those cases you will need to fragment the data in order to get through the smaller size networks.
-   The maximum size of a packet we are able to send is decieded by the MTU or Maximum Transmission Unit.
-   This designates the size of the data that we are able to send through the network without having to fragment any data
-   Fragmenting data slows down the flow of traffic in a network
-   losing a fragment loses an entire packet.
-   Requires overhead to chop up a packet and send it in pieces for it to be reassembled at the other side.

Its important to know the MTU all the way through the network from start to finish.
It's hard to know what the MTU is through each hop from point A to point B because each hop to each router is a different network with potentially different MTU's

-   Automated methods are often inaccurate
-   Especially when ICMP is filtered 

Building an Ethernet frame

DLC Header|IP Header | TCP Header | TCP Data      | FCS     |
14 bytes  | 20 bytes | 20 bytes   | 1460 bytes    | 4 bytes |
          |---------------------------------------| 
              *IP Packet Size: 1500 bytes*
The max size of a frame on an ethernet network is 1500 bytes


What is fragmentation?

Taking a single frame and splitting it up into multiple frames.

Fragments are always in multiples of 8 because of the number of fragmentation offset bits in the IP header.


MTU sizes are usually configured once
- Based on the network infrastructure and don't change often.

A significant concern for tunneled traffic
-  The tunnel may be smaller than your local Ethernet segment

What if you send packets with don't fragment (DF) set?
- Routers will respond back and tell you to fragment
- Hope you get the ICMP message.

Trouble shooting using ping.
to test the mtu of a network
- Ping with DF and force a maximum size of 1472 bytes
1500 bytes-8 byte ICMP header -20 bytes IP address = 1472 bytes
* Windows: ping -f -l 1472 8.8.8.8
* linux and macOS: ping -D -s 1472 8.8.8.8
-f : don't fragment
-l : length of data in bytes
8.8.8.8 : googles DNS server

