---
lastSync: Fri Mar 13 2026 09:08:51 GMT+0300 (Moscow Standard Time)
---
The power and speed of computer components has increased at a steady rate since desktop computers were first developed decades ago. Software makers create new applications capable of utilizing the latest advances in processor speed and hard drive capacity, while hardware makers rush to improve components and design new technologies to keep up with the demands of high-end software.

There's one element, however, that often escapes notice - the **bus**. Essentially, a bus is a channel or path between the components in a computer. Having a high-speed bus is as important as having a good transmission in a car. If you have a 700-horsepower engine combined with a cheap transmission, you can't get all that power to the road. There are many different types of buses.

The idea of a bus is simple -- it lets you connect components to the computer's processor. Some of the components that you might want to connect include hard disk, memory, sound systems, video systems and so on. You need special hardware to drive the screen, so the screen is driven by a graphics card. A graphics card is a small printed circuit board designed to plug into the bus. The graphics card talks to the processor using the computer's bus as a communication path.

The advantage of a bus is that it makes parts more interchangeable. If you want to get a better graphics card, you simply unplug the old card from the bus and plug in a new one. If you want two monitors on your computer, you plug two graphics cards into the bus. And so on.


## PCI History

The original PC bus in the original IBM PC (circa 1982) was 16 bits wide and operated at 4.77 MHz. It officially became known as the ISA bus. This bus design is capable of passing along data at a rate of up to 9 MBps (megabytes per second) or so, fast enough even for many of today's applications.

Several years ago, the ISA bus was still used on many computers. That bus accepted computer cards developed for the original IBM PC in the early 1980s. The ISA bus remained in use even after more advanced technologies were available to replace it.

There were a couple of key reasons for its longevity:

- Long-term compatibility with a large number of hardware manufacturers.
- Before the rise of multimedia, few hardware peripherals fully utilized the speed of the newer bus.

During the early 1990s, Intel introduced a new bus standard for consideration, the **Peripheral Component Interconnect** (PCI) bus. PCI presents a hybrid of sorts between ISA and VL-Bus. It provides direct access to system memory for connected devices, but uses a bridge to connect to the frontside bus and therefore to the CPU. Basically, this means that it is capable of even higher performance than VL-Bus while eliminating the potential for interference with the CPU.

![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Computer%20scheme.png?raw=true)
As processor speeds steadily climb in the GHz range, many companies are working feverishly to develop a next-generation bus standard. Many feel that PCI, like ISA before it, is fast approaching the upper limit of what it can do.

All of the proposed new standards have something in common. They propose doing away with the shared-bus technology used in PCI and moving to a **point-to-point switching connection**. This means that a direct connection between two devices (nodes) on the bus is established while they are communicating with each other. Basically, while these two nodes are talking, no other device can access that path. By providing multiple direct links, such a bus can allow several devices to communicate with no chance of slowing each other down.

HyperTransport, a standard proposed by Advanced Micro Devices, Inc. (AMD), is touted by AMD as the natural progression from PCI. For each session between nodes, it provides two point-to-point links. Each link can be anywhere from 2 bits to 32 bits wide, supporting a maximum transfer rate of 6.4 GB per second. HyperTransport is designed specifically for connecting internal computer components to each other, not for connecting external devices such as removable drives. The development of bridge chips will enable PCI devices to access the HyperTransport bus.