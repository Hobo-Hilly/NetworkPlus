Episode: Network Services
Learner Objectives:

Overview:

What is a network service?
In computer networking, a network service is an application running at the network application layer and above, that provides data storage, manipulation, presentation, communication or other capability which is often implemented using a client–server or peer-to-peer architecture based on application layer network protocols.[1]

Each service is usually provided by a server component running on one or more computers (often a dedicated server computer offering multiple services) and accessed via a network by client components running on other devices. However, the client and server components can both be run on the same machine.

Clients and servers will often have a user interface, and sometimes other hardware associated with it.


Examples
Examples are the Domain Name System (DNS) which translates domain names to Internet protocol (IP) addresses and the Dynamic Host Configuration Protocol (DHCP) to assign networking configuration information to network hosts. Authentication servers identify and authenticate users, provide user account profiles, and may log usage statistics.

E-mail, printing and distributed (network) file system services are common services on local area networks. They require users to have permissions to access the shared resources.

Other network services include:
Directory services
e-Mail
File sharing
Instant messaging
Online game
Printing
File server
Voice over IP
Video on demand
Video telephony
World Wide Web
Simple Network Management Protocol
Time service
Wireless sensor network

What is a Client?
A system or a program that requests the activity of one or more other systems or programs, called servers, to accomplish specific tasks. In a client/server environment, the workstation is usually the client.

What is a server?
A server is a computer program or device that provides a service to another computer program and its user, also known as the client. In a data center, the physical computer that a server program runs on is also frequently referred to as a server.


Explain the use and purpose of network services.

Description:

DHCP:
The Dynamic Host Configuration Protocol is a network management protocol used on Internet Protocol networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client–server architecture.

This is what we need to get them to connect to network iP address. Sub net mask, default Gateway.

EX:
DHCP Server                                                   DHCP Client
10.0.12.200/24        - - - ->   D(Discover)  - - - ->        10.?.?.??? 
                      <- - - -   O(Offer)     <- - - - 
                      - - - ->   R(Request)   - - - -> 
                      <- - - -   A(Acknowlege) <- - - - 

- Scope                                                     - 10.0.12.100    
- Exclusion ranges                                          - 255.255.255
- Reseravation                                              - 10.0.12.1
- Lease Time                                                - 8hr Lease    
- Scope Options
- Available Leases

Scope:
Is the Range of IP addresses that can be assigned.

Exclusion ranges:
The range of Ip Addresses NOT to be handed out

Reservation:
The reserved Ip Addresess that are used for broadcasting 1st and Last Ip Address which CANNOT be handed out either.

Dynamic assignment:
Means that when a device is connected it will get a new ip address from the range of Ip addresses that are ok to hand out.

Static assignment:
Usually for a specific device or device type (Printers,Firewalls, Switches, Routers) that will ALWAYS get the same IP address everytime it is connected to the network.

Lease time:
How long an IP address is good for that device on that network. After the expiration it will be handed a new valid IP address from the Range of acceptable/valid Ip addresses within the network.

Scope options:
A scope is a consecutive range of IP addresses that a DHCP server can draw on to fulfill an IP address request from a DHCP client. By defining one or more scopes on your DHCP server, the server can manage the distribution and assignment of IP addresses to DHCP clients.

Available leases:
A DHCP lease is a temporary assignment of an IP address to a device on the network. When using DHCP to manage a pool of IP addresses, each client served on the network is only “renting” its IP address. Thus, IP addresses managed by a DHCP server are only assigned for a limited period of time.

DHCP relay:
DHCP is a client server protocol that automatically provides IP hosts with IP addresses and other related configuration information. A DHCP relay (agent) is a host that forwards DHCP packets between clients and servers that are not on the same physical subnet.

EX:
                              (DHCP Relay)
10.0.12.200/24 
DHCP Server   10.0.12.1                          10.0.22.1        DHCP Client 
              255.255.255                        255.255.255                              
            = = = = = = = = = >      ROUTER     = = = = = = = >    ?  HOST computer   
                    R1(config) #interface GigabitEthernet0/1               - Ip Address          
                    R1(Config-if) #ip address 10.0.22.1 255.255.255.0      - Subnet Mask
                    R1(config-if) #ip helper-address 10.0.12.200           - Default Gateway
                                                                           - Lease

IP helper/UDP forwarding:
Internet Protocol Helper (IP Helper) assists network administration of the local computer by enabling applications to retrieve information about the network configuration of the local computer, and to modify that configuration.
NOTE: The IP helper-address. So instead of DHCP relay, which you might actually end up seeing, you might hear the term IP helper, those mean the exact same thing. If I have a client on another network that needs to get access to the DHCP server, I'm either going to need a DHCP relay or I'm gonna need the help of what an IP helper address.

So here once we do this, the DHCP client on this other network, what we can go ahead and we'll send a unit cast and set through the router to the DHCP server.  Now you might wanna well, the DHCP server is handing the 10.0.12 network addresses. You can set up another scope, which we had talked about previously. That can actually be for the 10.0.22 network. And it can figure it out. And then when it sends it back, is going to send back a unit cast over back to that DHCP client and also give you the same information that we would. So it actually does end up working for us now. both those are pretty much synonymous. Here one is setting up the actual true IP address. The term DHCP relay is usually setting up that logic like you need a relay, okay? Or you need a relay agent.

What's the context that we might see this one? Well, pretty much the idea of a branch office is actually key here that we might have a location, but we don't wanna set up another DHCP server over there. We just say everybody's gonna connect in and actually get a DHCP address from my DHCP server as well. So DHCP can be a bit dynamic.




When an RTP stream arrives at the router of your Studio, your Studio has to send the stream to the computer where your copy of LUCI Studio or a hardware codec is running. In the above example the computer has the IP-address 192.168.1.100 and is listening on port 5010. The incoming RTP stream at 5010 wants to go to this IP-address, but it doesn’t know the local IP-address. So the Router must be set to send the stream to port 5010 of the computer at 192.168.1.100.

Resource: https://technicadelarte.com/kb/?page_id=3229#:~:text=Port%20%3D%20source%20and%20destination%20number,the%20internet%20through%20a%20router.

This concept is called port-forwarding on your router.


DNS:
The Domain Name System is a hierarchical and distributed naming system for computers, services, and other resources in the Internet or other Internet Protocol networks. It associates various information with domain names assigned to each of the associated entities.

Record types

DNS Record	Description
A	           Maps domain names to IPv4 addresses
AAAA	       Maps domain names to IPv6 addresses
CNAME	       Redirects a domain to a different domain
PTR	           Resolves IPv4 or IPv6 addresses to domain names
NS	           Provides a list of the authoritative name servers responsible for the domain
MX	           Provides the domain names of mail servers that receive emails on behalf of a domain
SOA	           Provides important details about a DNS zone; required for every DNS zone
TXT	           Provides any type of descriptive information in text format


Resource:
https://bluecatnetworks.com/blog/know-the-eight-most-common-dns-records/

Root DNS servers:
A root name server is a name server for the root zone of the Domain Name System of the Internet. It directly answers requests for records in the root zone and answers other requests by returning a list of the authoritative name servers for the appropriate top-level domain

Internal vs. external

Zone transfers:
The process of replicating a zone file to multiple DNS servers is called zone transfer. Zone transfer is achieved by copying the zone file from one DNS server to a second DNS server. A main DNS server is the source of the zone information during a transfer. The main DNS server can be a primary or secondary DNS server.

Authoritative name servers:
Authoritative name server. An authoritative name server is a name server that gives answers in response to questions asked about names in a zone. An authoritative-only name server returns answers only to queries about domain names that have been specifically configured by the administrator.

Time to live (TTL):
Time to live or hop limit is a mechanism which limits the lifespan or lifetime of data in a computer or network. TTL may be implemented as a counter or timestamp attached to or embedded in the data. Once the prescribed event count or timespan has elapsed, data is discarded or revalidated.

DNS caching:
The DNS cache (also known as DNS resolver cache) is a temporary DNS storage on a device (your computer, smartphone, server, etc.) that contains DNS records of already visited domain names (A records for IPv4 addresses, AAAA records for IPv6, etc.). It keeps those records, depending on their time-to-live (TTL).

Reverse DNS/reverse lookup/forward lookup:
In computer networks, a reverse DNS lookup or reverse DNS resolution is the querying technique of the Domain Name System to determine the domain name associated with an IP address – the reverse of the usual "forward" DNS lookup of an IP address from a domain name.

Recursive lookup/iterative lookup:
A recursive DNS lookup is where one DNS server communicates with several other DNS servers to hunt down an IP address and return it to the client. This is in contrast to an iterative DNS query, where the client communicates directly with each DNS server involved in the lookup.

NTP:
The Network Time Protocol is a networking protocol for clock synchronization between computer systems over packet-switched, variable-latency data networks. In operation since before 1985, NTP is one of the oldest Internet protocols in current use. NTP was designed by David L. Mills of the University of Delaware.

Stratum
