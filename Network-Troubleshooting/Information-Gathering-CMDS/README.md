Topic: Network Troubleshooting Episode: Additional Command Learner Objectives:

Given a scenario, use the appropriate network software tools and commands.

Description:In this episode, the viewer will identify the command line tool tcpdump used to capture network traffic as well as the popular network mapping utility called nmap

Packet Capture with tcpdump
Start a basic capture
sudo tcpdump -i <interfacename>
sudo tcpdump -i ens33
Redirect capture data to text file
sudo tcpdump -i <interfacename> > test-cap.txt
sudo tcpdump -i ens33 > test-cap.txt
Analyzing captured data
less test-cap.txt
Creating an exportable PCAP file with tcpdump
sudo tcpdump -i <interfacename> -w test-cap.pcap
sudo tcpdump -i ens33 -w test-cap.pcap
Using nmap or Network Mapper
Basic scan of a single host
nmap <IP address>
Scan a network range without port discovery
nmap -sn <IP address-range> nmap -sn 10.0.99.99
+ Scan a range of IP addresses
nmap <IP address-range> nmap 10.0.99.1-254
+ Scan a single port
nmap -p <portnumber> <IP address> nmap -p 22 10.0.99.99
+ Scanning a port range
nmap -p <port range> <IP address> nmap -p 1-1023 10.0.99.99
+ Operating system detection
nmap -O <IP Address> nmap -O 10.0.99.99