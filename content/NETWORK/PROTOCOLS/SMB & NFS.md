---
lastSync: Wed Feb 11 2026 10:48:02 GMT+0300 (Moscow Standard Time)
---
# SMB

SMB (Server Message Block) is a network application-layer protocol that enables shared access to files, printers, ports, and other network resources between computers on a local network. Essentially, it is the foundation for collaboration in Windows networks.

Uses ports 445, 139

## Key Capabilities of SMB:

1.     Shared access to files and folders — the most well-known feature. You can share a folder on your PC, and other users on the network can read and write files in it (depending on permission settings).

2.     Printer sharing — allows multiple computers to print to a single network printer.

3.     Remote access to the file system — viewing and managing files on another computer as if they were local.

4.     Authentication and authorization — access control via usernames and passwords.

5.     Inter-process communication — used by some applications for data exchange over the network.

### Versions:

·         SMB1 (CIFS) — an old version from the 80s-90s. Slow, insecure (vulnerable to attacks, e.g., EternalBlue). In modern systems, it is recommended to disable it.

·         SMB2 — introduced with Windows Vista (2006). Significantly improved performance and security.

·         SMB3 — modern versions (starting from Windows 8 / Server 2012). Added:

o    Encryption on the fly (very important for security).

o    Enhanced fault tolerance.

o    Support for RDMA (accelerated data transfer for high-speed networks).

For work in mixed networks (with UNIX systems), the Samba protocol is used — the same SMB, but for Linux.

# NFS

NFS (Network File System) - was created by Sun Microsystems in 1984 as a stateful file-sharing protocol for Unix-based systems. Since then, NFS has had several updates. The latest version is NFS version 4 (NFSv4), developed by a working group from the Internet Engineering Task Force. NFS remains popular among Linux users.

Uses port 2049

The interaction process between client and server is largely similar to SMB — the differences lie in the details and mechanisms of operation. For example, in SMB, file systems are not mounted on the local SMB client. Instead, access to a network resource hosted on an SMB server is obtained via a network path.

Here’s how communication works between an NFS-enabled client and NFS server. First, a client requests a file or directory from the server using remote procedure calls (RPC). The server then checks the following:

·        The file or directory is available

·        The client has required access permissions

The server then mounts the file or directory remotely on the client and shares access via a virtual connection. For the client, NFS makes using the remote server file similar to accessing a local file during operations.

# Key Differences Between NFS and SMB

## **·       Shared Resources**

**SMB is designed for sharing a wide range of network resources, including file and print services, storage devices, and virtual machine storage. This differs from NFS, which only has built-in support for sharing files and directories.**

## **·       Client-to-Client Communication**

**SMB allows clients to communicate and share files with each other, using the server as an intermediary. NFS only permits client-server operations.**

**NFS can be used for the following scenarios:**

**·         You have a local network with all UNIX-based machines (including Linux-based environments) on the network.**

**·         You need to work with large-sized files.**

# Source: 
https://aws.amazon.com/compare/the-difference-between-nfs-smb/