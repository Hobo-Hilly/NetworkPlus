 Topic: Networking Fundamentals
Episode: IP Addressing Schemes
Learner Objectives:

Given a scenario, configure a subnet and use appropriate IP addressing schemes.

Description:

Public vs. private:
A public IP address is a unique IP address assigned to your network router by your internet service provider and can be accessed directly over the internet. A private IP address is a unique address that your network router assigns to your device. It is used within a private network to connect securely to other devices.

Class   Ranges                          Subnet Masks       Private Ranges           Subnet Masks 
A      | 0.0.0.1 - 127.255.255.255 |   | 255.0.0.0 |         |  10.0.0.0  |           |  255.0.0.0 |

B      | 128.0.0.1 -191.255.255.255 |   | 255.255.0.0 |      | 172.16.0.1-    |       | 255.240.0.0 | 
                                                             | 172.31.255.255 |            

C      | 192.0.0.1 - 223.255.255.255 |  | 255.255.255.0 |    | 192.168.0.1-    |      | 255.255.0.0 |
                                                             | 192.168.255.255 |

D      | 224.0.0.1 - 239.255.255.255 |

E      | 240.0.0.1 - 255.255.255.255 |

RFC1918

Network address translation (NAT):
We have to have a mechanism that allows us translate private IP addresses in the public IP addresses and that is NAT (Network Address Translation)

VLSM(Variable length subnet masking):
VLSM (Variable Length Subnet Mask) is a technique that allows network administrators to divide an IP address space into subnets of different sizes, rather than dividing it into subnets of the same size.

Port address translation (PAT)

IPv4 vs. IPv6

Automatic Private IP Addressing (APIPA)

Extended unique identifier (EUI-64)

Multicast

Unicast

Anycast

Broadcast

Link local

Loopback

Default gateway

IPv4 subnetting

Classless (variable-length subnet mask):
Now notice that there's not really technically here in classless addressing, we don't follow the rules of the sub net masks anymore. We can actually use class A, B or C addresses that's always signed out there on the internet for you, and then they can break it apart however they want to. We can now actually divide it up and we can have so many more networks that are actually much more suited to your space.

Class   Ranges                         
A      | 0.0.0.1 - 127.255.255.255 |   

B      | 128.0.0.1 -191.255.255.255 |   

C      | 192.0.0.1 - 223.255.255.255 |

D      | 224.0.0.1 - 239.255.255.255 |

E      | 240.0.0.1 - 255.255.255.255 |


Classful
We're going to actually end up doing here is we're gonna make some of these addresses that are not going to be available on the internet. We actually created what's called private IP addresses here. And those private ranges are good as long as they don't appear on the internet.

How does it work?
So what we'll do is we'll set up a network in which we use private IP addresses internally in our network. But then on the public on the internet facing side. Well actually use public IP addresses instead.

Class   Ranges                         Default Subnet Mask   Number of Networks   Num of Hosts/Network
A      | 0.0.0.1 - 127.255.255.255 |   | 255.0.0.0 |         |  126  |           |  16,777,214 |

B      | 128.0.0.1 -191.255.255.255 |   | 255.255.0.0 |      | 16,384 |          | 65,534 |   

C      | 192.0.0.1 - 223.255.255.255 |

D      | 224.0.0.1 - 239.255.255.255 |

E      | 240.0.0.1 - 255.255.255.255 |

Classless Inter-Domain Routing (CIDR) notation

IPv6 concepts

Tunneling

Dual stack

Shorthand notation

Router advertisement

Stateless address autoconfiguration (SLAAC)

Virtual IP (VIP) Subinterfaces
