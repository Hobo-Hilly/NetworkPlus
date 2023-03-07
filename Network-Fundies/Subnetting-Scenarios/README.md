These are some example scenarios for applying subnetting in the real world.

Subnetting Scenarios


Scenario #1: What is the broadcast Address for 223.209.177.136/29 network?  (Answer)223.209.177.135

What is the /29? On the end of an IPaddress they can express(Indicate) what the subnet mask is in bits using CIDR notation.

What is CIDR notation? (Classless Inter-Domain Routing) 
Definition:
CIDR notation compactly indicates the network mask for an address and adds on the total number of bits in the entire address using slash notation. For example, 192.168. 129.23/17 indicates a 17-bit network mask.

So the first thing you want to do when you get an IP address with a /XX on it is write out the subnet mask Immediately.

So 223.209.177.136/29
Each octet represents 8 bits. So we get 8 + 16 + 24 +1+1+1+1+1 = /29

              8   16 24  25,26,27,28,29 bits
Subnet Mask: 255.255.255.11111{000  host bits on right

So by converting the last octet looking at the CIDR notation we learn how many host bits are reserved for that particular network. With the knowlege of the HOST bits we can convert the last octet of the IpAddress in question and determine whether or not its a networkID IP Address or if its a Host/Node IpAddress being used on the network.


223.209.177.   136 == 10001{000  host bits on right. To get NetworkID host bits must all be 0's so .136 is the NetID

In this case we can see that converting the last octet of the IPaddress given leaves the last 3 bits as 0's so we know that 223.209.177.136 is in fact the NetworkID because to get the NetworkID the HOST/NODE bits must all be 000.  


So now in order to get the broadcast ID we know that we need to make the host portion of the last octet all 1's AND THEN you add the entire octet up! That will get you your broadcastID which as you can see below adds up to 143. So the BroadcastID for the network is 223.209.177.143

143 == 10001{111  To get the BroadcastID Host bits must be all 1's so .143 is the BroadcastID DO NOT FORGET TO CONVERT THE ENTIRE OCTET.

------------------------------------------------------------------------------------------


Scenario #2: What is the network ID for 221.230.76.99/27?
A.221.230.76.88/27
B.221.230.76.96/27  $
C.221.230.76.96/26
D.221.230.78.96/27

So to find a networkID we need to play with the network portion of the address we are given. The network bits are on the left of our binary version of the last octet.

221.230.76.___{00000

So we need to find out how many combinations of 2 we can make with 3 bits. Which is 2 to the power of 3. The number 2 comes from the fact that in binary we only use 1 or 0. So the combinations look like...

8 possibilities:
A. 000 ==  .0
B. 100 ==  .128 
C. 110 ==  .192
D. 111 ==  .224
E. 011 ==  .96  $
F. 001 ==  .32
G. 101 ==  .160
H. 010 ==  .64

So we see that the answer to the second question is 22.230.76.96/27.

-----------------------------------------------------------------------------------------

Scenario #3: You have 209.51.44.0/24, you need to subnet into 5 networks, what is your new subnet mask?
A.255.255.255.252
B.225.255.255.240
C.255.255.255.224
D.255.255.255.192

So based on what we learn if we increase the bits within the networks, the network portion, right. When we start to subnet, that means we get additional networks, right, if we increase the amount of bits that in the host portion we get more hosts, but we're looking at networks right now. So, I need to figure out how many bits does it take to get to 5 networks?

So I know that if we borrow one bit, that gives me two networks 0.0 and 0.128
If we borrow two bits to the power of two is gonna give me four possibilities.
If we borrow three bits which we would take to the power of two that will give us 8 possible networks.
So that means if we add/borrow 3 extra bits to the subnet mask we will have a /27.
Now we need to convert this into dot decimal notation.

255.255.255.000}00000

Since a subnet mask can only be all 1's the converstion would look like this

255.255.255.111 {00000  128 + 64 + 32 = 224

So the new subnet mask is 255.255.255.224. The answer is C!


Scenario #4: You want to covert 192.168.10.0/24 to binary. What represents that coversion?
A.10100000.10101000.00001010.00000000
B.11000000.11100000.00001010.00000000
C.11000000.10101000.00001100.00000000
D.11000000.10101000.00001010.00000000

If we use our binary table below we find that the answer is D! 

128  64  32  16  8  4  2  1  

11000000.10101000.00001010.00000000







Bonus:

Scenario #5: 191.199.67.97 255.255.248.0 is a host in which network?
A.191.199.64.0 255.255.248.0
B.191.199.0.0 255.255.248.0
C.191.199.32.0 255.255.248.0
D.191.199.16.0 255.255.248.0


Scenario #6: What is the broadcast ID for 191.199.67.97 255.255.248.0?
A.191.199.64.255    255.255.248.0
B.191.199.71.255    255.255.248.0
C.191.199.97        255.255.248.0
D.191.199.67.97     255.255.248.0


Scenario #7: how many hosts can 191.199.67.97/21 support?
A.2047	
B.2048
C.2046
D.2045

Scenario #8: What is the subnet mask and CIDR notation network that only needs 2 hosts per network?
A.255.255.255.253 and /30
B.255.255.255.252 and /21
C.255.255.255.254 and /31
D.255.255.255.252 and /30

----------------------------------------------------------------------------------

EXPLANATION

------------------------------------------------------------------------------------


Binary ANDing is the process of performing multiplication to two binary numbers. In the Decimal Numbering system, ANDing is addition: 2 and 3 equals 5. In Decimal, there are an infinite number of answers when ANDing two numbers together. However, in the Binary Numbering system, the AND function yields only two possible outcomes, based on four different combinations. These outcomes, or answers, can be displayed in what is known as a truth table:


          0 and 0 = 0
          1 and 0 = 0
          0 and 1 = 0
          1 and 1 = 1

You use ANDing most often when comparing an IP address to its subnet mask. The end result of ANDing these two numbers together is to yield the network number of that address.


192.168.100.115 == 11000000.10101000.01100100.01110011

255.255.255.192 == 11111111.11111111.11111111.11000000

    Binary ANDing
                   11000000.10101000.01100100.01000000

Convert back to dot decimal notation.

192.168.100.64
