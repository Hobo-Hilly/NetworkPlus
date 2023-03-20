Here I am going to design my own questions to use the Host's formula and the Subnet's formula.

Host's Formula == 2^h - 2
Two to the power of h minus 2. 
h: represents the number of 0's in the subnet mask, if the subnet mask were converted to binary.
-2: the minus 2 represents the first and last address. First Address is used to ID the network. Last Address is used as the broadcast address.

The hosts formula will tell you how many hosts will be allowed on a network that ALREADY has a certain subnet mask. 
KEY: you must have a subnet mask for this formula to work.


Subnet's formula == 2^s
two to the power of s.
s: the number of 1's added to the subnet mask, FROM what the submask was ORIGINALLY. 

The subnet's formula, which will ensure you have the right subnet mask for the number of subnets that you have. 
KEY: Just because you determine you have the right number of hosts for your LAN using the host's formula doesn't mean you'll have enough subnets for your network.

============================================================================================

The list of possible private ranges we will work with is as follows.

Address ranges to be use by private networks are:
Class A: 10.0. 0.0 to 10.255. 255.255.
Class B: 172.16. 0.0 to 172.31. 255.255.
Class C: 192.168. 0.0 to 192.168. 255.255.

---------------------------------------------------------------------------------------------

We are planning to use the ip block 192.168.0.0. Currently we have a small network of 40 hosts. But this will grow to 400 hosts within the next year. We also plan to have multiple locations of the same size in the future and need to enable them to communicate using this address space.

What subnet mask so I need to make this happen?

1. Determing a subnet mask to try out.
The simplest thing to do is to try out 255.255.255.0. This would give us 192.168.0.1 - 192.168.0.254 for hosts. Leaving 192.168.0.0 reserved for network ID and 192.168.0.255 reserved for the broadcast ID.

So since this is just a guess we need to apply the hosts formula to it and check to see if it will support our projected growth.

Convert the subnet to binary 255.255.255.0 == 11111111 11111111 11111111 00000000
Since there are 8 zeros in the subnet mask the host's formula would look like this 2^8 - 2 == 254 
So with this subnet mask we would only get 254 usable hosts. This fits our 40 hosts currently but wont meet our projections of 400.

2. So Adding 1s to the subnet mask means you get fewer hosts per network subnet but more network subnets. If you remove 1s from the subnet mask, you get more hosts per network but fewer networks. So to correct this problem we need to remove a one from the subnet mask to get more host availability.

So again our subnet mask looks like 255.255.255.0 == 11111111 111111111 11111111 00000000

so if we take away a 1 we get 11111111 111111111 11111110 00000000 which == 255.255.254.0

3. So now we have 9 zeros in the host portion of the subnet mask. So to find the new number of hosts allowed we would use the host formula again. 2^9 - 2 = 510. VICTORY! this will support our future projections of 400 hosts!

We now know the most efficient subnet mask for the network is 255.255.254.0. The valid host address range for each subnet must be written as two ranges.
The first IP subnet would be 192.168.0.1 through 192.168.0.255 and 192.168.1.0 through 192.168.1.254. Note that 192.168.0.0 identifies the subnet, and 192.168.1.255 is the network broadcast address.

That is how you arrive at the total of 510 usable hosts.




