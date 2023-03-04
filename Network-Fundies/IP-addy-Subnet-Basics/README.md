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
                110000000.10101000.00001010.


Step 2. Determine how many hostID bits to become networkID bits. 4 networks = _ bits?

"Since we need 4 networks we are only going to manipulate the first 2 spaces because there are only four possible value combinations in those two spaces; 00 / 10 / 01 / 11. Each combination represents a network ID. 4 combinations == 4 Networks

192.168.10.0 = 11000000.10101000.00001010.__000000
255.255.255.0 = 11111111.11111111.11111111.__000000

Conversion: 00 = .0
            10 = .128
            01 = .64
            11 = .192

Step 3. Change the subnet mask to associate new bits. So in the subnet mask we cannot have any 0's. Since we are only using 2 bits in the ip addressing we will follow suite with the subnet mask. So to do this we need to keep a continuous string of ones which would look like this ...

255.255.255.192 = 11111111.11111111.11111111. 11 {000000  The rest of this is now the host id. The value of two 1's in the last octet of the subnet mask would add up to {192} so now the subnet mask for this network is 
'255.255.255.192'


Step 4. find every possible binary combination of those 2 bits(we used in step 2) to become new NetworkIDs.


192.168.10.0 = 11000000.10101000.00001010.00000000
255.255.255.192 = 11111111.11111111.11111111.11000000

192.168.10.64 = 11000000.10101000.00001010.01   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000

192.168.10.128 = 11000000.10101000.00001010.10   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000

192.168.10.192 = 11000000.10101000.00001010.11   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000

So now at this point we have our 4 different Networks using the IP block given. We now need to look at the host ID and determine what the RANGE of addresses are going to be to get our 50 nodes per network.


Step 5. Determine the networkID 1st and Last valid address. As well as the BroadcastID/address

192.168.10.0 This is the network ID and the way we can tell that is the HOST portion of the IPaddress is ALL binary 0's. Like this... 
                                                HostID        
192.168.10.0 = 11000000.10101000.00001010.00   {000000

A. How do we get the first address?

To get the first address we look at the last octet in the networkID and turn the last value to a 1. Like this ..

192.168.10.0 = 11000000.10101000.00001010.0000000{1
So the 1st address in doted decimal is 192.168.10.1

NOTE: You cannot give the networkID (192.168.10.0) to a node. As it is already being used to identify the network.

B. How do we get the Last Address?

To get the Last address we look at the last octet in the networkID and change the last value to a 0 with all 1's behind it. Like this...
192.168.10.0 = 11000000.10101000.00001010.00{11111{0 == 192.168.10.62  
After adding the 5 1's in the last octet of the networkID and making the last value a 0 we get 192.168.10.62


C. How do we get the broadcastID? 

On EVERY SINGLE NETWORK there is whats known as a broadcastID and to get this we look at the networkID again and change the last octet(excluding the 2 bits that make up the networkID) to all 1's. Looks like this..

192.168.10.0 = 11000000.10101000.00001010.00 {111111 == 192.168.10.63

The broadcast network is what we use to make sure that we can send out/broadcast communications to every single device on the network. This is why it's reserved. "So that very first possibility isn't a possible address because everybody shares that. The last possibility isn't actually availabe it's an address but everybody shares it as well. So we're working in between."

192.168.10.63 is the Broadcast Network for the 192.168.10.0 network.


Administration
192.168.10.0 = 11000000.10101000.00001010.00   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000
1st address: 192.168.10.1
Last address: 192.168.10.62
BroadcastID: 192.168.10.63

Marketing
192.168.10.64 = 11000000.10101000.00001010.01   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000
1st address: 192.168.10.65
Last address: 192.168.10.126
BroadcastID: 192.168.10.127

Production
192.168.10.128 = 11000000.10101000.00001010.10   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000
1st address: 192.168.10.129
Last address: 192.168.10.200
BroadcastID: 192.168.10.201

Edutainers
192.168.10.192 = 11000000.10101000.00001010.11   {000000
255.255.255.192 = 11111111.11111111.11111111.11   {000000
1st address: 192.168.10.193
Last address: 192.168.10.254
BroadcastID: 192.168.10.255