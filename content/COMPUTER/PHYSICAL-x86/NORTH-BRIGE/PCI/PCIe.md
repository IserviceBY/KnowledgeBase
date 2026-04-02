---
lastSync: Wed Mar 25 2026 11:56:43 GMT+0300 (Moscow Standard Time)
---
Peripheral Component Interconnect (PCI) slots are such an integral part of a computer's architecture that most people take them for granted. For years, PCI has been a versatile, functional way to connect sound, video and network cards to a motherboard.

But PCI has some shortcomings. As processors, video cards, sound cards and networks have gotten faster and more powerful, PCI has stayed the same. It has a fixed width of 32 bits and can handle only 5 devices at a time. The newer, 64-bit PCI-X bus provides more bandwidth, but its greater width compounds some of PCI's other issues.

Fortunately, PCI Express (PCIe) eliminates a lot of these shortcomings, provides more bandwidth, and is compatible with existing operating systems.


## The Advantage of PCIe Devices

PCI Express is a serial connection that operates more like a network than a bus. Instead of one bus that handles data from multiple sources, PCIe has a switch that controls several point-to-point serial connections.

These connections fan out from the switch, leading directly to the devices where the data needs to go. Every device has its own dedicated connection, so devices no longer share bandwidth like they do on a normal bus.

When the computer starts up, PCI express slots determine which devices are plugged into the motherboard. It then identifies the links between the devices, creating a map of where traffic will go and negotiating the width of each link. This identification of devices and connections is the same protocol PCI uses, so PCIe does not require any changes to software or operating systems.

Each PCIe lane contains two pairs of wires — one to send and one to receive. Packets of data move across the lane at a rate of one bit per cycle. A x1 connection, the smallest PCIe link, has one lane made up of four wires. It carries one bit per cycle in each direction. A x2 link contains eight wires and transmits two bits at once, a x4 link transmits four bits, and so on. Other configurations are x12, x16 and x32.

## PCI Express Connection Speeds

The 32-bit PCI bus has a maximum speed of 33 MHz, which allows a maximum of 133 MB of data to pass through the bus per second. The 64-bit PCI-X bus has twice the bus width of PCI. Different PCI-X specifications allow different rates of data transfer, anywhere from 512 MB to 1 GB of data per second.

A single PCIe lane, however, can handle 200 MB of traffic in each direction per second. A x16 PCIe connector can move an amazing 6.4 GB of data per second in each direction. At these speeds, a x1 connection can easily handle a gigabit Ethernet connection as well as audio and storage applications. A x16 connection can easily handle powerful graphics adapters.

## Source: 
https://computer.howstuffworks.com/pci-express.htm