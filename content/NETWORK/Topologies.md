---
lastSync: Wed Feb 25 2026 12:02:07 GMT+0300 (Moscow Standard Time)
---
# Important Points

Network Topology is important because it defines how devices are connected and how they communicate in the network. Here are some points that defines why network topology is important.

- ****Network Performance:**** Upon choosing the appropriate topology as per requirement, it helps in running the network easily and hence increases network performance.
- ****Network Reliability:**** Some topologies like Star is reliable as if one connection fails, it provide an alternative for that connection, hence it works as a backup.
- ****Network Expansion**** : Choosing correct topology helps in easier expansion of Network as it helps in adding more devices to the network without disrupting the actual network.
- ****Network Security:**** Network Topology helps in understanding how devices are connected and hence provides a better security to the network.
# Star Topology

In Star Topology, all the devices are connected to a single hub through a cable. This hub is the central node and all other nodes are connected to the central node. The hub can be passive in nature i.e., not an intelligent hub such as broadcasting devices, at the same time the hub can be intelligent known as an active hub. Active hubs have repeaters in them.
![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Star%20topology.png?raw=true)
## Advantages of Star Topology

- If N devices are connected to each other in a star topology, then the number of cables required to connect them is N. So, it is easy to set up.
- Each device requires only 1 port i.e. to connect to the hub, therefore the total number of ports required is N.
- It is Robust. If one link fails only that link will affect and not other than that.
- Easy to fault identification and fault isolation.
- Star topology is cost-effective as it uses inexpensive coaxial cable.

## Disadvantages of Star Topology

- If the concentrator (hub) on which the whole topology relies fails, the whole system will crash down.
- The cost of installation is high.
- Performance is based on the single concentrator i.e. hub.


# Bus Topology

Bus Topology is a network type in which every computer and network device is connected to a single cable. It is bi-directional. It is a multi-point connection and a non-robust topology because if the backbone fails the topology crashes.
![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Bus%20topology.png?raw=true)
## Advantages of Bus Topology

- If N devices are connected to each other in a bus topology, then the number of cables required to connect them is 1, known as backbone cable, and N drop lines are required.
- Coaxial or twisted pair cables are mainly used in bus-based networks that support up to 10 Mbps.
- The cost of the cable is less compared to other topologies, but it is used to build small networks.
- Bus topology is familiar technology as installation and troubleshooting techniques are well known.
- CSMA/CD was the only MAC method used in traditional bus Ethernet. Modern switched Ethernet does not use CSMA/CD because full-duplex operation eliminates collisions.

## Disadvantages of  Bus Topology

- A bus topology is quite simpler, but still, it requires a lot of cabling.
- If the common cable fails, then the whole system will crash down.
- If the network traffic is heavy, it increases collisions in the network. To avoid this, various protocols are used in the MAC layer known as Pure Aloha, Slotted Aloha, CSMA/CD, etc.
- Adding new devices to the network would slow down networks.
- Security is very low.


# Ring Topology

In a Ring Topology, it forms a ring connecting devices with exactly two neighboring devices. A number of repeaters are used for Ring topology with a large number of nodes, because if someone wants to send some data to the last node in the ring topology with 100 nodes, then the data will have to pass through 99 nodes to reach the 100th node. Hence to prevent data loss repeaters are used in the network.

In-Ring Topology, the Token Ring Passing protocol is used by the workstations to transmit the data where, Token passing is a network access method in which a token is passed from one node to another node & Token is a frame that circulates around the network.
![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Ring%20topology.png?raw=true)
## Operations of Ring Topology

- One station is known as a monitor station which takes all the responsibility for performing the operations.
- To transmit the data, the station has to hold the token. After the transmission is done, the token is to be released for other stations to use.
- When no station is transmitting the data, then the token will circulate in the ring.

## Advantages of Ring Topology

- The data transmission is high-speed.
- The possibility of collision is minimum in this type of topology.
- Cheap to install and expand.

## Disadvantages of Ring Topology

- The failure of a single node in the network can cause the entire network to fail.
- Troubleshooting is difficult in this topology.
- Less secure.

# Tree Topology

Tree topology is the variation of the Star topology. This topology has a hierarchical flow of data. In Tree Topology, protocols like DHCP and SAC (Standard Automatic Configuration) are used.
![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Tree%20topology.png?raw=true)
## Advantages of Tree Topology

- It allows more devices to be attached to a single central hub thus it decreases the distance that is traveled by the signal to come to the devices.
- It allows the network to get isolated and also prioritize from different computers.
- We can add new devices to the existing network.

## Disadvantages of Tree Topology

- If the central hub gets fails the entire system fails.
- The cost is high because of the cabling.
- If new devices are added, it becomes difficult to reconfigure.

# Hybrid Topology

Hybrid Topology is the combination of all the various types of topologies we have studied above. Hybrid Topology is used when the nodes are free to take any form. It means these can be individuals such as Ring or Star topology or can be a combination of various types of topologies seen above. Each individual topology uses the protocol that has been discussed earlier.
![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Hybrid%20topology.png?raw=true)
## Advantages of Hybrid Topology

- This topology is very flexible.
- The size of the network can be easily expanded by adding new devices.

## Disadvantages of Hybrid Topology

- It is challenging to design the architecture of the Hybrid Network.
- Hubs used in this topology are very expensive.
- The infrastructure cost is very high as a hybrid network requires a lot of cabling and network devices.

# Source: 
https://www.geeksforgeeks.org/computer-networks/types-of-network-topology/