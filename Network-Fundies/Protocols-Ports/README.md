Episode: Protocols and Ports
Learner Objectives:

Explain common ports and protocols, their application, and encrypted alternatives

Description:In this episode, the viewer will identify common TCP and UDP protocols as well as the ports associated with each. Also, the viewer with examine IP protocol type identifiers.

What are protocols?
In general, protocol essentially is a set of rules for communication. For instance in client server networks that we have clients that are asking for resources and servers that are providing those resources. When a host asks for those resources, it's going to ask (depending on the resource that being asked for), it's going to ask it in a certain language. And that's the rule, the structured mean for communications.

What are ports and why do we use them?
Applications identify which communication application is performing and they identify those logical endpoints through the port values, the port numbers. 

Summary:
So protocols, a structure rule set of rules for communication, pork values allows applications to identify logical endpoints of connections.

File Protocols:
FTP (File Transfer Protocol) 20/21  Written in the 70s
TFTP (Trivial File Transfer Protocol) 69   UDP version of FTP 
SFTP ( Secure File Transfer Protocol) 22    FTP tunneled through SSH
SMB (Server Message Block) 445      Window sharing Resources

Remote Connections:
SSH (Secure Shell) PORT# 22 Encrypted Remote Connection
Telnet PORT# 23 Unsecured Plain text
RDP (Remote Desktop Protocol) PORT# 3389

PORT#

Email:
SMTP (Simple Mail Transfer Protocol) PORT# 25  Outbound mail: used for sending outbound emails

POPv3 (Post Office Protocol version 3) PORT# 110  Inbound email: used for receiving inbound email
Application- you can pull all your emails down to that computer and it erases all the emails off of the server it was being hosted on. So you wont have access to it from another computer. 

IMAP(Internet Message Access Protocol) PORT# 143  Inbound email

Application- it allows u to loging to an IMAP server and manage your emails. EX: Gmail, Ymail, outlook. You can go to an computer loging to the webinterface and manage your emails on that server.

Secure E-mail protocols:
So with these email variants we can stop people from eavesdropping on our email communications. These variants use Transpot Layer Security to Encrypt Inbound and Outbound communications between the Client and the Server themselves.

SMTPS (Simple Mail Transfer Protocol Secure) PORT# 587 (TLS)
IMAPS (Internet Message Access Protocol Secure) PORT# 993 (SSL)
POP3S (Post Office Protocol version 3 Secure) PORT# 995 (SSL)


Websites
Application: Remember that http, unsecure unencrypted if you will https secure or encrypted. And it's the way we make the communications between a web browser client and the web server. Remember that websites are written in html. And the http protocol allows the web server to deliver that website over the network and then the browser on the client site renders it and we get hopefully a lovely web page.

HTTP(Hyper Text Transfer Protocol) PORT# 80
HTTPS(Hyper Text Transfer Protocol Over SSL(Weak-Old)/ TLS(Strong/Latest)) PORT# 443
SSL:Secure Socket Layer
TLS: Transport Layer Security


SQL related
SQL Server PORT# 1433
SQLNet PORT# 1521
MySQL PORT# 3306


Network Services

DHCP (Dynamice Host Configuration Protocols) PORT# 67/68 The client Communicates(Hands out Ip addresses) with the server over port# 67 and the server communicates back to the client on port# 68

DNS (Domain Name Systems) uses PORT# 53 Allows us to take FQDN's (fully qualified domain names) and map them to IP addresses over Port# 53

NTP (network time protocol) PORT# 123 Time is very, very important. NTP makes sure that time is synchronized and that's where NTP network time protocol comes in. 

SNMP (Simple Network Management Protocol) PORT#'s 161/162. This is a client server type communication. We have an agent, there are devices are going to communicate with the management station over port 161 and the management station communicates back to the devices over port 162. This allows us to manage all network devices from one server.


When we have to interact with directory service based servers, we can do it in an unsecure manner or we can do it in a secure manner. We do it in an unsecure manner. It's gonna be over port 389 It's called the lightweight directory access protocol. If we do it in a secure manner, right? Encrypted communication. It's gonna be port 636

LDAP (lightweight directory access protocol) PORT# 389 

LDAPS (lightweight directory access protocol secure) PORT# 636

Syslog PORT# 514 Syslog is a way to collect logging information on your various devices. 


SIP (Sessions Initiaition Protocol) PORT#'s (Unencrypted) 5060 / (Encrypted) 50611
Application: this is used for Real-time video, voice, messaging signaling

---------------------------------------------------------------------------------

Where do we get all these port numbers from?
These are allocated to server services by the Internet Assigned Numbers Authority (IANA)

IP protocol types

Internet Control Message Protocol (ICMP)
That is from a standards body called the internet assigned numbers authority. IANA 

PORT RANGE
0-1023 these ports are "well known" and require admin or SUDO privileges to access or communicate with. That means these are identified services, established services, common services that are used within networking.

1024-49,151 are considered Registered Ports. This is where things like RDP if you will and sip fall into and that's between 1024 to 49,151.

49,152-65,535 When we get on the higher end of these port ranges, 49,152 all the way out to 65,535. These are called dynamic ports. They're also called private ports. And you've also, we'll also see in documentation them called ephemeral ports. 

What does that mean? 
That means my computer can use them at its will and then once that port is no longer used it goes right back into the pool and they can computers can use them again to it's how we keep track of things like multiple connections if you will to using if you will even sometimes the same service.


What is a protocol Identifier?

What an IP protocol type does, is it identifies within that IP. Layer essentially what the encapsulated upper layer protocol is. 

ICMP (Internet Control Message Protocol):
This is how when we send ping packets as well, learn with troubleshooting and some of the network tools. This is for network communications and troubleshooting. This has a protocol identifier of 1.

IGMP (Internet Group Message Protocol):
That's for multicast communications. That's a protocol identifier of 2.

TCP (Tranmission Control Protocol) That's a protocol identifier of 6.

UDP (User Datagram Protocol) That's a protocol identifier of 17

Generic Routing Encapsulation (GRE) That's a protocol identifier of 47.

Then we have a couple that are used for IP. Sec, a group or a suite of security protocols for IP. There is one known as the encapsulating security payload and authentication header and you'll see the protocol identifiers of 50 and 51. Again it just identifies the upper layer protocols at the IP. 

Internet Protocol Security (IPSec)

ESP(Encapsulating Security Payload) - 50

AH (Authentication Header) - 51