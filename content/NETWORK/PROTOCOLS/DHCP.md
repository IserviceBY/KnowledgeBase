---
lastSync: Mon Mar 02 2026 09:50:31 GMT+0300 (Moscow Standard Time)
---
Dynamic Host Configuration Protocol is a network management protocol that is used to dynamically assign the IP address and other information to each host on the network so that they can communicate efficiently. DHCP automates and centrally manages the assignment of IP address easing the work of network administrator. In addition to the IP address, the DHCP also assigns the subnet masks, default gateway and domain name server(DNS) address and other configuration to the host and by doing so, it makes the task of network administrator easier.

**Components of DHCP**

1. ****DHCP Server:**** It is typically a server or a router that holds the network configuration information.
2. ****DHCP Client:**** It is the endpoint that gets the configuration information from the server like any computer or mobile.
3. ****DHCP Relay Agent:**** If you have only one DHCP Server for multiple LAN’s then the DHCP relay agent present in every network will forward the ****DHCP request**** to the servers. This because the DHCP packets cannot travel across the router. Hence, the relay agent is required so that DHCP servers can handle the request from all the networks.
4. ****IP address pool:**** It contains the list of IP address which are available for assignment to the client.
5. ****Subnet Mask:**** It tells the host that in which network it is currently present.
6. ****Lease Time:**** It is the amount of time for which the IP address is available to the client. After this time the client must renew the IP address.
7. ****Gateway Address:**** The gateway address lets the host know where the gateway is to connect to the internet.


**How do DHCP works?**

DHCP works at the application layer to dynamically assign the IP address to the client and this happens through the exchange of a series of messages called DHCP transactions or DHCP conversation.

- ****DHCP Discovery:**** The DHCP client broadcast messages to discover the DHCP servers. The client computer sends a packet with the default broadcast destination of ****255.255.255.255**** or the specific subnet broadcast address if any configured. 255.255.255.255 is a ****special broadcast address****, which means “****this network****”: it lets you send a broadcast packet to the network you’re connected to.
- ****DHCP Offer:**** When the DHCP server receives the DHCP Discover message then it suggests or offers an IP address(form IP address pool) to the client by sending a DHCP offer message to the client. This DHCP offer message contains the proposed IP address for DHCP client, IP address of the server, MAC address of the client, subnet mask, default gateway, DNS address, and lease information.
- ****DHCP Request:**** In most cases, the client can receive ****multiple DHCP offer**** because in a network there are many DHCP servers(as they provide fault tolerance). If the IP addressing of one server fails then other servers can provide backup. But, the client will accept only one DHCP offer. In response to the offer, the client sends a ****DHCP Request**** requesting the offered address from one of the DHCP servers. All the other offered IP addresses from remaining DHCP servers are withdrawn and returned to the pool of IP available addresses.
- ****DHCP Acknowledgment:**** The server then sends Acknowledgment to the client confirming the DHCP lease to the client. The server might send any other configuration that the client may have asked. At this step, the IP configuration is completed and the client can use the new IP settings.


Source:
https://afteracademy.com/article/what-is-dhcp-and-how-does-it-work