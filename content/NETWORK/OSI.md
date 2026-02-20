---
lastSync: Fri Feb 20 2026 09:08:15 GMT+0300 (Москва, стандартное время)
---
The Open Systems Interconnection (OSI) model — is a conceptual model that divides network communication and interoperability into seven abstract layers. It provides a standardized model that enables different applications, computer systems and networks to communicate.
![[Pasted image 20260212143845.png]]


The OSI model emerged as a solution to communication incompatibilities between the diverse array of networking protocols in use around the turn of the century. The layers of OSI gave developers and engineers a framework for building interoperable hardware and software across networks by providing a categorical approach to networking.

The layers are:

- **Layer 7:** The application layer initiates communication with the network, including the protocols and data manipulation processes that convert computer-readable network data into user-readable responses.

- **Layer 6:** The presentation layer prepares data for the application layer, including data translation, compression and encryption.

- **Layer 5:** The session layer initiates and terminates connections between two devices interacting on the network, making sure that resources are neither overused nor underutilized.

- **Layer 4:** The transport layer transmits end-to-end data between two devices interacting on the network, making sure that data isn’t lost, misconfigured or corrupted.

- **Layer 3:** The network layer handles data addressing, routing and forwarding processes for devices interacting across different networks. If the devices are on the same network, they don’t need the network layer to interact.

- **Layer 2:** Unlike the network layer, the data link layer manages data routing between two interacting devices on the same network.

- **Layer 1:** The physical layer comprises the physical assets, like routers and USB cables, that convert data into strings of 1s and 0s for transmission to higher layers.