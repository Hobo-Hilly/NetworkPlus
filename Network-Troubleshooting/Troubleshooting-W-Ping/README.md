Showname: Network+ (N10-008) 
Topic: Network Troubleshooting 
Episode:Troubleshooting with ping Learner Objectives:
Given a scenario, use the appropriate network software tools and commands.

Description:In this episode, the viewer will identify the best practices when using the command ping to test end-to-end communications over networks.

Troubleshooting steps using ping
Ping the loopback address
ping 127.0.0.1

Ping the local host's IP address
ping <hostIPAddress>
ping 10.0.14.53

Ping another host on the local network
ping 10.0.99.99

Ping the default gateway
ping <gatewayIPAddress>

Ping remote host
ping <RemoteHostIPAddress>
ping 4.2.2.2
ping 8.8.8.8
ping 8.8.4.4

Persistant Pings in Windows (Not applicable to *Nix-based systems)
ping <IPAddress> -t
ping 4.2.2.1 -t

--------------------My Notes -------------------------------

The five steps that we talk about are pinging first which known as the loopback address.

