filename:comptia-netplusn10008-5--1-ip-addressing-commands Showname: Network+ (N10-008) Topic: Network Troubleshooting Episode: IP Addressing Commands

Learner Objectives:

Given a scenario, use the appropriate network software tools and commands.

Description:In this episode, the viewer will identify the command line tools used to troubleshooting IP addressing such as Windows ipconfig and Linux-based ifconfig, ip as well as the route command.

Windows

- Using ipconfig:
ipconfig
ipconfig /all

- Forcing IPv4 and IPv6 address release:
ipconfig /release

- Intiating DHCPv4 and DHCPv6 lease process:
ipconfig /renew
ipconfig /renew6


Linux IP Configuration Commands

- Display IP information:
ip a
ip addr
ip addr show

- Release DHCP address:
dhclient -r
Configure IP address and subnet mask
ip addr add 10.0.200.100/16 dev ens33

- Verify connectivity:
ping 127.0.0.1
ping IP address of local machine
ping node on same network
ping default gateway
ping remote host

- Configure default gateway:
ip route add default via <IP address> dev <devicename>
Verify default gateway
ip route show
 + Installing *ifconfig* and *route*
 ```
apt install net-tools ```

- Release IP address:
dhclient -r

- Configure IP address with ifconfig:
ifconfig <devicename> <IP address/netmask>

- Add default gateway:
route add default gw <gateway address>

- Verify connectivity:
ping 4.2.2.1