Topic: Network Troubleshooting Episode: Additional Command Learner Objectives:

Given a scenario, use the appropriate network software tools and commands.

Description:In this episode, the viewer will identify the command line tools used to troubleshoot communications such as netstat and arp.

Windows systems
Using netstat to display all connections
netstat -a
Do not perform name resolution
netstat -n
Displaying connection with detailed statisics
netstat -s
Determine process associated with conection
netstat -o
Using arp to display ARP table
arp -a
Adding a static ARP entry
arp -s <IP address> <MAC address>
arp -s 10.0.200.200 c4-d6-55-3d-a8-4a
Verify static ARP entry
arp -a
Delete static ARP entry
arp -d <IP address> <MAC address>
arp -d 192.168.0.10 c4-d6-55-3d-a8-4a
Linux Systems
Listing all TCP and UDP port
netstat -a | more
Listing all TCP connections
netstat -at
Listing statistics by protocol
netstat -s
    ```
+ Displaying the ARP table
---BSD style--- arp -a ---Linux style--- arp -e
Adding static ARP entry
sudo arp -s <IPAddress> <MACAddress> sudo arp -s 10.0.200.200 c4-d6-55-3d-a8-4a
- Verifying static ARP entry
arp -e
- Delete a static ARP entry
arp -d <IP address> <MAC address> arp -d 192.168.0.100 c4-d6-55-3d-a8-48

Basic network platform commands
show interface
show config
show route