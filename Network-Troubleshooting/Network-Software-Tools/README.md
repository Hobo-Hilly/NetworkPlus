Network+ (N10-008) Topic: 
Network Troubleshooting 
Episode: 
Network Software Tools 
Learner Objectives:
Given a scenario, use the appropriate network software tools and commands.

Description:In this episode, the viewer will identify the software-based application used to troubleshoot network communications.

Software tools
- WiFi analyzer
In Windows 10, you can just get this one right out of the Microsoft store, it's completely free and it's got a lot of bells and whistles. Just remember what a wifi analyzer one of its purposes. It helps us to kind of find out, to inspect what our current settings if you will within our wireless network, we can check out things like signal strength

It lets us know what the current signal strength is as it appears to this wireless network adapter, remember it from the perspective of my wireless adapter inside of this machine.

We can see what the service identifier is, we can see the channel that it's operating on. We also see what the bandwidth is, the protocol 802.1x, Service Set Identifier which looks just like a mac address (SSID), IP details. We can see additional security information; what security it is using and what mose it's in. EX: Infrastructure mode versus Ad-hoc mode.

Summary:
So the wire wifi analyzer is a very good tool to gain insight into configuration signal strength within your wireless networks. Normally, the reason why we end up using these tools is kind of key. Normally if somebody has an issue with the wireless and we're not sure if the issue is with that one particular access point or multiple access point, is there something going wrong with the overall connection itself? Does the user actually have the right SS ID? Are they actually on the right network or they on a congested channel? All this tool actually really does help us to be able to do some of that analysis and then figure out a plan of attack on what we can change or what we shouldn't change. 

- Protocol analyzer/packet capture(Wireshark)
Remember the packet capture functionality a lot of time is build in to the same application, and that just means I can actually grab those packets off the network, put them in a container, right? But then if I got this boxes container, I don't actually know what's in the container, I have to open it up and I have to inspect what we just put in the box, and that's the protocol analysis.

Summary:
Have a basic context of where we would use this packet capture and protocol analyzer if I wanna inspect the traffic that's going on in the network. From the point of the perspective of this network adapter, this is the utility that we would use.

- Bandwidth speed tester
I like speakeasy is you can say, hey, I wanna tell which server I wanna do a speed test against because you'll see when you have multi geographical locations to where your information is traveling. Sometimes on the East Coast, you're fine but then sometimes on the West Coast it's not so good, right?

 I like to be able to measure speed test from multiple locations. And we can just basically start this test and it's going to send information and I can see our IP address and I can see that it's going out of our provider here and it's going to a server somewhere in Atlanta Georgia there.(They are in Gainesville Florida)

Now you can also have these on your local machine too, right? For instance, since I'm in Windows 10 I'm just gonna go ahead and I could run one here as well and this again is not going out to the internet to connect. And this is really good if you need to do some kind of bandwidth speed test within your network, right? I don't have to have an ISP connection here, I can connect to a connectivity device and if I wanted to measure the speed between my self and that device I could. So these are very, very good for the overall testing of the bandwidth within your networks and pasture networks.

- Port scanner
We talked about the port scanner of 'Nmap' being able to see ports, there are other ones out there too. So for instance this is land sweeper kind of gives you a way that you can find all of the hosts that are online within your networks. And we've talked about doing that as well with something like a Nmap of the network mapper as well.

- iperf

- NetFlow analyzers:
Net flow analyzers allow us to do things like for instance bandwidth monitoring and bandwidth analysis as well. 
We get a good graphical read out here. We can look at the devices within our networks as well as things like for instance, we can do maps as well too. So you can kind of see, you know, what are the devices, how is your network infrastructure currently set up, right? Are you running virtual machines? Right? Going farther across WAN links too

Netflow kind of won these big, gigantic protocols that's out there, they can relay a ton of information that can be helpful and useful and also help you to troubleshoot.


RESOURCE: https://www.paessler.com/prtg/prtg-network-monitor 30Day Trial with unlimited sensors then it drops down to 90 sensors.
(Passer Router Traffic Grabber)

- TFTP server

- Terminal emulator

- IP scanner




