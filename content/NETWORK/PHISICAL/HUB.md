---
lastSync: Mon Mar 02 2026 10:09:36 GMT+0300 (Moscow Standard Time)
---
A hub is a multi-port repeater. A hub connects multiple wires coming from different branches, for example, the connector in star topology which connects different stations. Hubs cannot filter data, so data packets are sent to all connected devices.  In other words, the collision domain of all hosts connected through hub remains one. Hub does not have any routing table to store the data of ports and map destination addresses., the routing table is used to send/broadcast information across all the ports.

**How Does a Network Hub Work?**

A hub is a multiport device, which has multiple ports in a device and shares the data to multiple ports altogether. A hub acts as a dumb switch that does not know, which data needs to be forwarded where so it broadcasts or sends the data to each port. 

Suppose there are five ports in a hub A, B, C, D, and E. Consider A wants to send any data frame, or let's say A is acting as a sender, so the hub will forward the data transmitted by A to B, C, D, E. Now, at the same time B also wants to send the data then data received from A and B will collide and can cause data loss. In this situation, the data gets destroyed, and the hosts send a jam signal to all the hosts informing them about the collision, and each sender needs to wait for a certain amount of time. 

## Types of Network Hubs

Networks hubs are classified into three types:

1. ****Active Hub:**** They have a power supply for regenerating, and amplifying the signals. When a port sends weak signalled data, the hub regenerates the signal and strengthens it, then send it further to all other ports. Active hubs are expensive in costs as compared to passive hubs. 
2. ****Passive Hub:**** Passive hubs are simply used to connect signals from different network cables as they do not have any computerised element. They simply connect the wires of different devices in the star topology. Passive hubs do not do any processing or signal regeneration and that's why do not require electricity the most they can do is they can copy or repeat the signal. It can't clean the message, and it can't amplify or strengthen the signal. 
3. ****Intelligent Hub:**** Intelligent hubs as the name suggests are smarter than active and passive hubs. The intelligent hub comprises a special monitoring unit named aManagement Information Base (MIB). This is software that helps in analysing and troubleshooting network problems. Intelligent hubs work similarly to active hubs but with some management features. Like it can monitor the traffic of the network and the configuration of a port.


## Difference Between Network Hub And Switch

| Hub                                                                                                  | Switch                                                                               |
| ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| It works on the physical layer of the OSI model.                                                     | It works on the data link layer of the OSI.                                          |
| It performs frame flooding, which includes broadcast, multicast and unicast as well.                 | It mainly performs broadcasts and performs multicast, and unicast whenever required. |
| The transmission mode is half-duplex.                                                                | The transmission mode is full-duplex.                                                |
| It cannot perform data filtering.                                                                    | It can filter data and send the frame to the desired destination.                    |
| There is no spanning tree.                                                                           | A switch may contain more than one spanning tree possible.                           |
| It can not store the MAC address of the ports and the destination address of the frame that arrived. | It can store the data in a routing table it helps in further sending the data.       |
| It is a passive device.                                                                              | It is an active device.                                                              |
| Hub can operate at a speed of 10Mbps.                                                                | The switch can operate at a speed of 10-100Mbps and 1- 10 Gbps.                      |


## Source: 
https://www.geeksforgeeks.org/computer-networks/what-is-network-hub-and-how-it-works/