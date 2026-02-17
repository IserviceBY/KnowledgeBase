---
lastSync: Wed Feb 11 2026 11:04:58 GMT+0300 (Moscow Standard Time)
---
The Network Time Protocol (NTP) is a system for synchronizing the clocks of hosts and clients across the Internet. NTP is a protocol intended to synchronize all computers participating in the network to within a few milliseconds of Coordinated Universal Time (UTC). The core of the protocol is NTP’s clock discipline algorithm that adjusts the local computer’s clock time and tick frequency in response to an external source — such as another trusted NTP server, a radio or satellite receiver, or a telephone modem. A core problem in NTP is establishing the trust and accuracy of nodes in the NTP network. This is done through a combination of selection and filtering algorithms to choose from the most reliable and accurate peer in the synchronization network. NTP is running on millions of servers and clients across the world to keep accurate time on devices throughout the Internet.


**NTP Network Architecture**

NTP uses a hierarchical network architecture that forms a tree structure. Each level of this hierarchy is called a _stratum_ and is assigned a number starting with zero representing reference hardware clocks. A level one server is synchronized with a level zero server, and this relationship continues so that a server synchronized to a stratum nn server runs at stratum n+1n+1. The stratum number therefore represents the distance from an accurate reference clock. In general, the stratum of a node in the server is an indication of quality and reliability but this is not always the case; it is common to find stratum three time sources that are higher quality than other stratum two time sources.

![[Pasted image 20260211110347.png]]

Stratum 0

These are high-precision timekeeping devices such as atomic clocks, GPS or other radio clocks. They generate a very accurate time signal that is directly connected to a connected computer. Stratum 0 devices are also known as reference clocks. NTP servers cannot advertise themselves as stratum 0.

Stratum 1

These are computers that are directly attached to stratum 0 devices. Their system time is synchronized to within a few microseconds of their attached devices. Stratum 1 servers may peer with other stratum 1 servers for sanity check and backup. They are also referred to as primary time servers.

Stratum 2

These are computers that are synchronized over a network to stratum 1 servers. Often a stratum 2 computer queries several stratum 1 servers and selects the most accurate time representation from them. Stratum 2 computers may also peer with other stratum 2 computers to provide more stable and robust time for all devices in the peer group.

Stratum 3

These are computers that are synchronized to stratum 2 servers. They employ the same algorithms for peering and data sampling as stratum 2, and can themselves act as servers for stratum 4 computers, and so on.

And this hierarchy continues up to stratum 15. The following figure depicts the hierarchical nature of the NTP system. Reference clocks at the top of the hierarchy are accurate time pieces and stratum 1 are computers directly attached to those time pieces. From there, increasing strata numbers indicate where each computer synchronizes time data from.


Source: 
**https://sookocheff.com/post/time/how-does-ntp-work/**