filename:comptia-netplusn10008-5--1-dns_troubleshooting_commands Showname: Network+ (N10-008) Topic: Network Troubleshooting Episode: Network Command Line Tools Learner Objectives:

Given a scenario, use the appropriate network software tools and commands.

Description:In this episode, the viewer will identify the command line tools used to troubleshooting the DNS service such as nslookup and ipconfig in Windows as well as dig in Unix and Linux systems.

- Windows DNS Commands:
nslookup is the default command line utility
Two modes (interactive and non-interface)
Determining locally configured DNS server(s)

 - ipconfig /all:
Interactive mode using configured DNS server

- nslookup itpro.tv:
Interactive mode using another DNS server

- nslookup itpro.tv 4.2.2.3:
Interactive mode using local DNS server and another DNS Server
nslookup
itpro.tv
itpro.tv 4.2.2.2

- Query DNS for detailed information:
set debug
itpro.tv
set nodebug
set d2
itpro.tv
set nod2

- Querying DNS server for specific records:
set type=soa
itpro.tv
set type=aaaa
itpro.tv
google.com

- Display local resolver cache:
ipconfig /displaydns

- Flushing the local resolver cache:
ipconfig /flushdns

- Linux DNS commands:
nslookup is in Linux but has been deprecated
Domain Internet Groper or dig is the primary DNS utility
Identifying locally configure DNS servers
systemd-resolve --status

- Determining if dig is present:
dig -v

- Installing *dig:
sudo apt install dnsutils \(Debian/Ubuntu\)
sudo yum install bind-utils \(RHEL/CentOS\)

- Querying DNS with dig with local DNS server:
dig itpro.tv

- Querying DNS with another DNS server:
dig @4.2.2.3 itpro.tv

- Querying DNS server for specific record types:
dig itpro.tv MX
dig itpro.tv NS

- Reducing the amount of data returned by DNS server:
dig itpro.tv +short

- Querying DNS server for detailed information:
dig itpro.tv +noall +answer

- List each server the DNS query goes through to the final destination:
dig itpro.tv +trace