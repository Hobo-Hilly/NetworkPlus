Showname: Network+ (N10-008) Topic: Networking Fundamentals
Episode: Datacenter Network Architecture Learner Objectives:

Explain basic corporate and datacenter network architecture.

Description:

Three-tiered
    Core
    Distribution/aggregation layer
    Access/edge

Software-defined networking
    Application layer
    Control layer
    Infrastructure layer
    Management plane

Spine and leaf
    Software-defined network
    Top-of-rack switching
    Backbone

Traffic flows
    North-South
    East-West

Branch office vs. on-premises datacenter vs. colocation

Storage area networks
    Connection types
    Fibre Channel over Ethernet (FCoE)
    Fibre Channel
    Internet Small Computer Systems Interface (iSCSI)

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