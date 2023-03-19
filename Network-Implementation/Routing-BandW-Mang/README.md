Topic: Network Implementations Episode: Routing and Bandwidth Management Learner Objectives:

Compare and contrast routing technologies and bandwidth management concepts.

Description: Routing is a very important topic, because essentially it's what allows us to communicate off of our local area networks. 

Routing:
Routing is the process of path selection in any network. A computer network is made of many machines, called nodes, and paths or links that connect those nodes. Communication between two nodes in an interconnected network can take place through many different paths.


Dynamic routing:
Dynamic routing is a mechanism through which routing information is exchanged between routers to determine the optimal path between network devices. A routing protocol is used to identify and announce network paths.

Protocols:

RIP:
Routing Information Protocol (RIP) is a distance-vector routing protocol. Routers running the distance-vector protocol send all or a portion of their routing tables in routing-update messages to their neighbors. You can use RIP to configure the hosts as part of a RIP network.

OSPF:
Open Shortest Path First is a routing protocol for Internet Protocol networks. It uses a link state routing algorithm and falls into the group of interior gateway protocols, operating within a single autonomous system. 

EIGRP:
Enhanced Interior Gateway Routing Protocol (EIGRP) is a network protocol that enables routers to exchange information more efficiently than earlier network protocols, such as Interior Gateway Routing Protocol (IGRP) or Border Gateway Protocol (BGP).

Border Gateway Protocol BGP:
BGP (Border Gateway Protocol) is the protocol underlying the global routing system of the internet. It manages how packets get routed from network to network through the exchange of routing and reachability information among edge routers.

Link state vs. distance vector vs. hybrid

Static routing:
A static route is a pre-determined pathway that a packet must travel to reach a specific host or network. Some ISPs require static routes to build your routing table instead of using dynamic routing protocols. Static routes do not require CPU resources to exchange routing information with a peer router.

Default route:
A default route defines where packets will be sent if no specific route for the destination network is listed in the routing table. If no default route is set, the router will discard all packets with destination addresses not found in its routing table.

Administrative distance:
Administrative distance (AD) or route preference is a number of arbitrary unit assigned to dynamic routes, static routes and directly-connected routes. The value is used in routers to rank routes from most preferred (low AD value) to least preferred (high AD value).

Exterior vs. interior

Time to live:
Time to live (TTL) refers to the amount of time or “hops” that a packet is set to exist inside a network before being discarded by a router. TTL is also used in other contexts including CDN caching and DNS caching.

Bandwidth management:
1. Bandwidth management is the process of measuring and controlling the communications on a network link, to avoid filling the link to capacity or overfilling the link, which would result in network congestion and poor performance of the network. 

2. Bandwidth management or bandwidth control is the process of regulating the amount of data on a network by setting allocations to every data-consuming application and device on the network. It helps alleviate network congestion or bottlenecks and ensures enough bandwidth for critical applications within an organization.

Traffic shaping:
Traffic shaping (or packet shaping) is a technique of limiting the bandwidth that can be consumed by certain applications to ensure high performance for critical applications.

Quality of service (QoS):
Quality of service (QoS) is the use of mechanisms or technologies that work on a network to control traffic and ensure the performance of critical applications with limited network capacity. It enables organizations to adjust their overall network traffic by prioritizing specific high-performance applications.

QoS is typically applied to networks that carry traffic for resource-intensive systems. Common services for which it is required include internet protocol television (IPTV), online gaming, streaming media, videoconferencing, video on demand (VOD), and Voice over IP (VoIP). 

How Does QoS Work?
QoS networking technology works by marking packets to identify service types, then configuring routers to create separate virtual queues for each application, based on their priority. As a result, bandwidth is reserved for critical applications or websites that have been assigned priority access. 

QoS technologies provide capacity and handling allocation to specific flows in network traffic. This enables the network administrator to assign the order in which packets are handled and provide the appropriate amount of bandwidth to each application or traffic flow.

Types of Network Traffic
Understanding how QoS network software works is reliant on defining the various types of traffic that it measures. These are:

Bandwidth: The speed of a link. QoS can tell a router how to use bandwidth. For example, assigning a certain amount of bandwidth to different queues for different traffic types.
Delay: The time it takes for a packet to go from its source to its end destination. This can often be affected by queuing delay, which occurs during times of congestion and a packet waits in a queue before being transmitted. QoS enables organizations to avoid this by creating a priority queue for certain types of traffic.
Loss: The amount of data lost as a result of packet loss, which typically occurs due to network congestion. QoS enables organizations to decide which packets to drop in this event.
Jitter: The irregular speed of packets on a network as a result of congestion, which can result in packets arriving late and out of sequence. This can cause distortion or gaps in audio and video being delivered.
