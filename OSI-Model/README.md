This is section 1.1 in the Network+ exam objectives

All : Application Layer
People  : Presenation Layer
Seam    : Session   Layer
To  : Transport Layer
Need    : Network Layer
Data    : Data Link Layer
Processing  : Physical Layer



OSI model

Layer 7 - Application Layer
This is the Layer we as Humans get to see. When we fireup chrome firefox or anyweb browser to start a session. Our home page comes back to us and
that is an example of us looking at The application layer of the OSI model which is layer 7.  
EX: If your transferring a file with FTP.
    If your doing name resolution with DNS  
    If your using a browser with HTTP or HTTPS.
        If you are doing any of these things you are using/interacting with an application (layer 7) protocol               
- End User layer
- HTTP, FTP, IRC, SSH, DNS

Layer 6 - Presentation Layer
This is where the data is taken and manipulated into a form we can understand. Like a pretty google home page.
This layer does all of the Character encoding and decoding.
This layer also handles the encryption and decryption of data
This layer is often combind with the application layer 7
- Syntax layer
- SSL, SSH, IMAP, FTP, MPEG, JPEG

Layer 5 - Session Layer
This layer is designed to start and stop communication between one end point and another.
This is where control protocols and tunneling protocols happen to begin and end communication from one device to antoher.
- Synch & send to port
- API's, Sockets, WinSock

Layer 4 - Transport Layer This is the post office layaer.
This determines how and where data will enter a system.
- End-to-end connections
- TCP,UDP
Transmission Control Protocol
User Datagram Protocol

Layer 3 – Network Layer 
The routing layer. It is associated with IP addresses. 
This is where Frames will be broken up into fragments
- Packets
- IP,ICMP,IPsec,IGMP


Layer 2 – Data Link Layer or "The Switching Layer" 
- Frames
- Ethernet, PPP, Switch, Bridge
- Switching EX: Communication based on MAC addresses of Media Access Control. MAC address to MAC address.
This moves Data Frames
The basic network "Language"
    - the foundation of the communication at the data link layer.
Data Link Contorl (DLC) protocols
    -MAC(Media Access Control) address on Ethernet
    MAC addresses or Layer Two addresses


Layer 1 – Physical Structure
Coax, Fiber, Wireless, Hubs, Repeaters
- The physics of the network
    - Signaling, cabling, connectors
    - This layer isn't about protocols
- If you have a physical layer problem
    - Fix your cabling, punch downs etc...
    - Run loopback tests, test/replace cables,
    swap adapter cards


A conversation...
Each time you open an application of send traffic over the network we can describe this in the context of the osi model as follows...


1. We login and open gmail.com at https://mail.google.com  : this is the data at layer 7
    - As we use the application on the screen we are at the Application Layer in the OSI model
2. Everything being communicated back and forth to the google server and your browser is being encrypted at the next layer
which is the Presentation Layer. Layer(6)
3. Now here at the Session Layer it is going to link everything above at the Presentation Layer and the Application layer to the information below it. 
    - this layer is Layer(5) which passes the data down to the Transport Layer.0
4. Here at Layer(4) the Transport Layer. Will deceide that we are using TCP in this case so the Data will be encapsulated via the TCP protocol
5. Here we are now at the Network Layer. This is where IP encapsulation will occur.
6. The packet is encapsulated again within Layer 2 or the Data Link layer which turns the packet into a Frame. The frame is then ready to be
traverse a network and go from hop to hop.
7. The data is now at the Physical layer and ready to be converted into electrical signals. Could be binary data or analog data. 

