Topic: Network Troubleshooting Episode: Network Command Line Tools Learner Objectives:

Given a scenario, use the appropriate network software tools and commands.

Windows
Display local routing table
route print ```
Forcing IPv4 or IPv6
route print -4
route print -6
Add a route
route add <networkID> mask <netmask> <gateway address> route add 10.2.0.0 mask 255.255.0.0 gateway 10.0.14.58 ```
Add persistent route
route add <networkID> mask <netmask> <gateway address> route add -p 2.0.0 mask 255.255.0.0 gateway 10.0.14.58 ```
Deleting a route
route delete <networkID> route delete 10.2.0.0 ```
Simple route trace
tracert itpro.tv ```
Route tracing without name resolution
tracert -d itpro.tv ```
Linux
Displaying local routing table
ip route list
ip r
or
route


Adding a route
ip route add <networkID/cidr mask> via <gateway address> dev <devicename>
ip route add 10.2.0.0/16 via 10.0.14.35 dev ens33
ip route add 10.3.0.0/16 via 10.0.14.35 dev ens33
or
route add -net <networkID/cidr mask> gw <gateway address>
route add -net 172.16.100.0/24 gw 172.16.100.1


Deleting a route
ip route delete <networkID/cidr mask> via <gateway address> dev <devicename>
ip route delete 10.2.0.0/16 via 10.0.14.35 dev ens33
ip route delete 10.3.0.0/16 via 10.0.14.35 dev ens33
or
route delete -net <networkID/cidr mask> gw <gateway address>
route delete -net 172.16.100.0/24 gw 172.16.100.1


Determine if traceroute is installed
traceroute --version
Installing traceroute
Debian/Ubuntu
sudo apt install traceroute -y
RHEL/CentOS
sudo yum install traceroute -y
Simple route trace
traceroute itpro.tv
Force IPv4 or IPv6 trace
traceroute -4/6 <destination host>
traceroute -4 <itpro.tv>
Simple route trace
mtr itpro.tv