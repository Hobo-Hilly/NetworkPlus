This is going to be all about how and why we use subnetting. 

Why do we use subnetting?
Subnetting divides broadcast domains so traffic is routed efficiently, improving speed and network performance. A subnet mask ensures that traffic remains within its designated subnet. This reduces major congestion and reduces the load imparted on the network.


Scenario:

There are 4 departments and there are 50 hosts per department. We only have the 192.168.10.0 block of ip addresses to work with. How do we set this up?

Using VLSM(Variable Length Subnet Masking)

Starting Point:

Network  {192.168.10.0}   1 network; 254 hosts
Subnet mask {255.255.255.0}

Variable Length Subnet Masking

4 departments, 50 hosts per department
Answer:

192.168.10.0            192.168.10.128
255.255.255.192         255.255.255.192

192.168.10.64           192.168.10.192
255.255.255.192         255.255.255.192

What is subnetting?
Subnetting is just a common division problem using binary numbers. The process is the same as a common division problem.
EX:
100/4 = 25

-----------------------------------------------------------------------------------------------------

Scenario: We are assigned the 192.168.10.0 ip range with a subnet mask of 255.255.255.0. We need to subnet to create 4 networks that can have 50 hosts/nodes per network. One for each of the 4 departments.


How did we get the answer?
EX: We get there is 5 steps.

Step 1. Convert to binary
192.168.10.0 = 11000000.10101000.00001010.00000000
255.255.255.0 = 11111111.11111111.11111111.00000000












