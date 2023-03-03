This Episode of Notes is about IPv4 Addressing

What is IPv4?

Definition:
Internet Protocol version 4 is the fourth version of the Internet Protocol. It is one of the core protocols of standards-based internetworking methods in the Internet and other packet-switched networks. IPv4 was the first version deployed for production on SATNET in 1982 and on the ARPANET in January 1983.

- 32 bit binary number (A string of 1's and 0's thats 32 bit long)

- Reported in 'Dotted decimal notation' with a subnet mask
EX:
    ip address    192.168.10.1  'dotted decimal'  
    NOTE: 
    This is a representation of the 32 bit binary number
    
    subnet mask   255.255.255.0  'This is a 24 bit subnet mask'
    NOTE: 
    The subnet mask; in binary, is what shows us what portion of those 32 bits is gonna represent our network ID and what portion is gonna represent our host ID

- 2 parts to an IP address + subnet mask makes 3

                  (1)          (2)
               network ID    Host ID/AKA:Node ID
ip address    {192.168.10}    {.1}


    (3)
subnet mask   255.255.255.0
NOTE:
The purpose of the subnet mask is to let us know what network range we are on. A subnet mask is used to divide an IP address into two parts. One part identifies the host (computer), the other part identifies the network to which it belongs. "If you don't apply a subnet mask, nobody can tell what the network ID. That's its purpose is to let us know what network were on."

What does this all look like in Binary?

               network ID    Host ID/AKA:Node ID
ip address    {192.168.10}    {.1}
subnet mask   255.255.255.0


               Network ID                Host ID
              192.       168.     10.        1 
ip address  {11000000.10101000.00001010} {.00000001}

                Network ID                 Host ID
              255.      255.     255.        0
subnet mask {11111111.11111111.11111111} {.00000000}
              32-bit binary 
NOTE: The dotes are here to help us understand in all actuallity we would not see any dotes at all. The 32-bit binary above are exact translations of the ip address and the subnet mask above. Each number in the IP address and subnet mask is referred to as an octet. This is because if they are written in binary there are 8 place values in each block seperated by dots/ written in dot decimal notaion. 

How does the conversion process work?
Method #1

128  64  32  16  8  4  2  1  The top number represents the value of each place holder/space in the binary octet
 1   1   1   1   1  1  1  1  Starting at the far end of the octet(Place holder 8) the value is halved until we get to the last place holder/space 1. which is equal to one. 

