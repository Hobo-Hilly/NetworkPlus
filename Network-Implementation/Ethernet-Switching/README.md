Topic: Network Implementations Episode: Ethernet Switching Learner Objectives:

Given a scenario, configure and deploy common Ethernet switching features.

Description:

Data virtual local area network (VLAN):
A virtual local area network (VLAN) is a virtualized connection that connects multiple devices and network nodes from different LANs into one logical network.

Voice VLAN:
The voice VLAN feature enables access ports to carry IP voice traffic from an IP phone. When the switch is connected to a Cisco 7960 IP Phone, the phone sends voice traffic with Layer 3 IP precedence and Layer 2 class of service (CoS) values, which are both set to 5 by default.

Port configurations:
The Port Configuration window displays the port configuration and provides access to a window for modifying port configuration. Port configuration values are: Port. Slot and port number for each port installed in the switch (for example, A1 means the first port in slot A).

Port tagging/802.1Q:
The purpose of a tagged or "trunked" port is to pass traffic for multiple VLAN's, whereas an untagged or "access" port accepts traffic for only a single VLAN. Generally speaking, trunk ports will link switches, and access ports will link to end devices./

802.1q:
IEEE 802.1Q is the networking standard that supports Virtual LANs (VLANs) on an Ethernet network. The standard defines a system of VLAN tagging for Ethernet frames and the accompanying procedures to be used by bridges and switches in handling such frames.

Port aggregation:
Ethernet port aggregation between two devices allows your devices to treat multiple Ethernet links as if they were a single link. Combining two network connections for LAN aggregation allows you to increase network bandwidth and provide network redundancy between your router and a client device if one link fails.

Link Aggregation Control Protocol (LACP):
Defined within IEEE 802.3ad, the Link Aggregation Control Protocol (LACP) is a standards-based method to control the bundling of several physical network links together to form a logical channel for increased bandwidth and redundancy purposes.

Duplex:
Duplex is a bidirectional communication system that allows both end nodes to send and receive communication data or signals, simultaneously and one at a time. Both nodes have the ability to operate as sender and receiver at the same time, or take turns sending or receiving data.

Speed:
Speed refers to the maximum rate you can transmit data, typically measured as megabits per second (Mbps). Bandwidth refers to the maximum amount of data your connection can handle at any moment, also measured as Mbps (and increasingly Gbps, for gigabyte connections).

Flow control:
In data communications, flow control is the process of managing the rate of data transmission between two nodes to prevent a fast sender from overwhelming a slow receiver. Flow control should be distinguished from congestion control, which is used for controlling the flow of data when congestion has actually occurred.

Port mirroring:
Port mirroring is used on a network switch to send a copy of network packets seen on one switch port (or an entire VLAN) to a network monitoring connection on another switch port.

Port security:
Port Security helps secure the network by preventing unknown devices from forwarding packets. When a link goes down, all dynamically locked addresses are freed. The port security feature offers the following benefits: You can limit the number of MAC addresses on a given port.

Jumbo frames:
Jumbo frames are packets that are longer than the standard Ethernet (IEEE 802.3) frame size of 1,518 bytes. The frame size definition for jumbo frames is vendor-specific because jumbo frames are not part of the IEEE standard. The most commonly used jumbo frame size is 9,018 bytes.

Auto-medium-dependent interface crossover (MDI-X):
Auto-MDIX configures the cable connection automatically, allowing both crossover and straight-through cabling to be used. When the Auto-MDIX interface is connected, it will correct any improper cabling. To ensure the speed is correct, the duplex setting needs to be set to "auto.” Advertisements.

MAC address tables:
The MAC address table is where the switch stores information about the other Ethernet interfaces to which it is connected on a network. The table enables the switch to send outgoing data (Ethernet frames) on the specific port required to reach its destination, instead of broadcasting the data on all ports (flooding).

PoE/PoE+:
Power over Ethernet (PoE) is a technology for implementing wired Ethernet local area networks (LANs) that enables the electrical current necessary for operating each device to be carried by Ethernet data cables instead of standard electrical power cords and wiring./

PoE+:
The updated IEEE 802.3at-2009 PoE standard, also known as PoE+ or PoE plus, allows for up to 30 W of power to Type 2 devices. That's sufficient power for devices such as VoIP phones, wireless access points, and security cameras.


Spanning Tree Protocol:
The Spanning Tree Protocol is a network protocol that builds a loop-free logical topology for Ethernet networks. The basic function of STP is to prevent bridge loops and the broadcast radiation that results from them.

CSMA/CD:
CSMA/CD (Carrier Sense Multiple Access with Collision Detection) helps hosts to decide when to send packets on a shared network segment and how to detect collisions if they occur. For example, in a hub network, two devices can send packets at the same time. This can cause a collision.

Address Resolution Protocol (ARP):
The Address Resolution Protocol is a layer 2 protocol used to map MAC addresses to IP addresses. All hosts on a network are located by their IP address, but NICs do not have IP addresses, they have MAC addresses. ARP is the protocol used to associate the IP address to a MAC address.

Neighbor Discovery Protocol:
The Neighbor Discovery Protocol (NDP), or simply Neighbor Discovery (ND), is a protocol of the Internet protocol suite used with Internet Protocol Version 6 (IPv6).[1] It operates at the link layer of the Internet model,[2][3] and is responsible for gathering various information required for network communication, including the configuration of local connections and the domain name servers and gateways.[4]

The protocol defines five ICMPv6 packet types to perform functions for IPv6 similar to the Address Resolution Protocol (ARP) and Internet Control Message Protocol (ICMP) Router Discovery and Router Redirect protocols for IPv4. It provides many improvements over its IPv4 counterparts (RFC 4861, section 3.1). For example, it includes Neighbor Unreachability Detection (NUD), thus improving robustness of packet delivery in the presence of failing routers or links, or mobile nodes.