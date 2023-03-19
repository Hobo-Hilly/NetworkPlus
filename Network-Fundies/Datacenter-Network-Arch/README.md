Showname: Network+ (N10-008) Topic: Networking Fundamentals
Episode: Datacenter Network Architecture Learner Objectives:

Explain basic corporate and datacenter network architecture.

Description:

Three-tiered
    Core:
    The core layer that is just a high speed data network itself. Really not a lot of things are actually configured here is designed as she say, how much data can I pump through this entire network at this level to ensure that the access that's actually provided is the same over on one end of it.
    
    Distribution/aggregation layer:
    Here is where we apply policies and different things that we want to control the data as it goes through or the traffic that goes through here, we have what's called the distribution layer as well.

    
    Access/edge:
    This is the lowest tier/level of the 3 tiers. It represents connected devices like a laptop,desktop,phone,tablet.

NOTE: So this is actually good in small to medium size is but after a while we see that it's not super efficient for really high density environments such as True datacenters.

Spine and leaf
    Software-defined network
    Top-of-rack switching
    Backbone

The actual spine devices that we have up here at the top, there are actually connected to each of the leaf devices, but notice that the spine devices are not directly connect to each other nor the leaf devices connected to each other.

So what is this architecture about? It allows us to actually expand the capabilities of our datacenter in two different ways.


Software-defined networking
    Application layer
    Control layer
    Infrastructure layer
    Management plane


Traffic flows
    North-South:
North-south refers to the traffic that flows in and out of a datacenter. For example, traffic from an application to a backend service. This type of traffic is a typical target for attack vectors because it flows over the public internet.
    
    East-West:
    In computer networking, east-west traffic is network traffic among devices within a specific data center.

Branch office vs. on-premises datacenter vs. colocation

Storage area networks(SAN)
Connection types:

    Fibre Channel over Ethernet (FCoE):
    Fibre Channel over Ethernet is a computer network technology that encapsulates Fibre Channel frames over Ethernet networks. This allows Fibre Channel to use 10 Gigabit Ethernet networks while preserving the Fibre Channel protocol
    
    Fibre Channel:
    Fibre Channel is a high-speed data transfer protocol providing in-order, lossless delivery of raw block data. Fibre Channel is primarily used to connect computer data storage to servers in storage area networks in commercial data centers.
    
    Internet Small Computer Systems Interface (iSCSI):
    Internet Small Computer Systems Interface or iSCSI is an Internet Protocol-based storage networking standard for linking data storage facilities. iSCSI provides block-level access to storage devices by carrying SCSI commands over a TCP/IP network.

=================================================================================

Corporate Network Architecture

On-Premises:
It's a single geographical location, right? And it's gonna be something that's maintained by our company. the key here, of course, is that is the ownership is ours, from the idea of the implementation of it to of course, the managing of it to the breakdown. Everything that's actually on it is going to be what we're actually going to do. So we wanna make sure that it's set up to be accessible from our network. We wanna make sure of course, that all of the network architecture is there for us to be able to do the management that we need to. And actually take advantage of the best speed that we can to provide the data that we need to our entire network.

- This is all LAN infrastructure so its going to be maintained on Local Area Networks.

Branch Office:
when you start incorporating a branch office, now I'm thinking we're gonna have two LANs. And we're gonna have connections going over carrier based networks with WLAN's as well. We're gonna have to be paying an ISP, if you will, to help us to maintain the connectivity is but it's typically a remote location. now what we have is really kind of a mixture of things, right? We not only have maybe a small storage device in a branch office. But we also of course have the users there, we have everything and they're probably gonna be connected that single network.

Datacenter:
Once we get to a certain size, we need an entire network that is dedicated to the idea of moving and storing of all the data that we need. This is the idea of a data center. data centers can go from gigantic data centers, like he's talked about here, Amazon, Google, Facebook, you name it, all those bigger places and they literally have locations. All they do are running server farms, that's essentially all that they're doing. And they're not really hosting anybody sitting there at computers using and accessing those data actually distributed all across the world as well. 


Colocation:
Colocation (sometimes known as “colo”) is the practice of renting space for your servers and other computing hardware at a third-party provider's data center facility. When the company doesn't have the space power and other resources to store all of the data neccessary we look for companies to rent from. They say. "Hey, We have the space and what I'm willing to do, I'm willing to rent you that. 

So I'll allow you to buy your own servers to put everything that you need to in this particular rack here and use the power and do all that. All that will be metered for us so that we know exactly how much to charge you and how to do that. But then we'll have a connection for you and it's dedicated to you connecting in, so you can use that as if it's at your network, even though it's actually in my place. So they're essentially renting us a box or a location so that we can actually put our servers there and not have to actually move to a brand new building

What is a datacenter?
Definition:
A data center or data centre is a building, a dedicated space within a building, or a group of buildings used to house computer systems and associated components, such as telecommunications and storage systems.

They house Critical Applications and infrastructure like Servers, storage, routers, switches, firewalls, and controllers. These systems are optimized to enable delivery of data and applications.

Explanation:
One of the things I think about as how can we make all of these devices work together to provide that and we can use something like a distributed operating system to be able to optimize. Now what I mean by distributed operating system is let's talk about a local operating system. It runs the hardware on my laptop, Ronnie's got an operating system, it runs the hardware on his laptop. They do not sit here and talk together and run each other's hardware. Distributed operating system. That datacenter says, hey, this operating system is going to run all of your servers. It's going to run everything in that data center to deliver that data in those applications.

Key Understanding:
So when it comes down to the idea of a datacenter, key elements are actually involved in that center. One is redundancy. The ability to actually maintain all the up time that we need. Also, of course the power management and the cooling facilities as well, machines get hot. We have to ensure that they can actually be cooled and providing a dedicated datacenter where that can actually be monitored and changed as needed is also going to be part of it too, help optimize even better as long as we actually get high speed data too. We talk about structured cabling and the management of those so that we don't have a spider web or a bird's nest of cables running everywhere. But what we have is truly structured cabling that helps out everything that we need to and of course the density of the environment and we can put a lot more in a single location to be able to help us out in what we're actually doing.