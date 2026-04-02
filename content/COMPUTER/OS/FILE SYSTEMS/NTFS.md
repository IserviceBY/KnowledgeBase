---
lastSync: Mon Mar 23 2026 16:21:31 GMT+0300 (Moscow Standard Time)
---
NTFS, which stands for NT file system and the New Technology File System, is the file system that many versions of the Windows and Windows Server operating systems (OSes) use for storing, organizing, and retrieving files on hard disk drives (HDDs) and solid-state drives (SSDs).

NTFS is the primary file system for recent versions of Windows and Windows Server OSes. A computer's OS creates and maintains the file system on a storage drive or device. The file system essentially organizes the data into files. It controls how data files are named, stored, retrieved and updated and what other information can be associated with the files -- for example, data on file ownership and user permissions.

With Windows 2008, Microsoft introduced self-healing NTFS, which means that the file system can automatically correct transient corruption issues without taking the volume offline. Also, if a computer restarts after a system failure, NTFS automatically restores data using the log file and checkpoint information.

**How NTFS works**

The OS determines which file system will be used. For example, NTFS is the default file system for Windows 10/11 and for all versions of Windows Server after version 2016. But older versions of Windows -- Windows NT, Windows 95, Windows 98, Windows 2000 -- support either HPFS or FAT file systems.

When an HDD is formatted or initialized, it is divided into partitions. Partitions are the major divisions of the hard drive's physical space. Within each partition, the OS keeps track of all the files it stores. Each file is stored on the HDD in one or more clusters or disk spaces of a predefined uniform size. A cluster refers to the smallest unit of size that the NTFS can reference when accessing storage

In NTFS, cluster sizes range from 4 kilobytes (KB), which is the default size, to 2048 KB. NTFS supports different combinations of cluster sizes and volumes. For example, a 4 KB cluster can have a maximum volume of 16 TB, while the maximum volume for a 2048 KB cluster can be as high as 8 PB.

Cluster size and deployment often determine system performance. In general, higher cluster sizes offer increased volume and file capacity. This can be a big advantage when a volume holds many large files, and in situations involving the use of Hyper-V, Structured Query Language or deduplication. On the other hand, smaller clusters can be used to minimize wasted space when storing small files. That said, Microsoft discourages the use of clusters smaller than 4 KB.

## NTFS features

- **Quick file access.** NTFS uses a binary tree directory scheme to index files and keep track of file clusters. This allows for efficient file sorting, organization, and retrieval.
- **File size.** NTFS supports very large files, with maximum allowable volumes of 16 TB.
- **Continuously available volumes**. NTFS can be used with the CSV file system in Windows Server failover clusters to enable multiple cluster nodes to access continuously available volumes simultaneously.
- **User permissions.** NTFS has an access control list that lets a server administrator control who can access specific files and the access type.
- **Compression.** Integrated file compression shrinks file sizes and provides more storage space.
- **Unicode file naming.** Because it supports file names based on Unicode, long file names can be used with a wider array of characters. Short names can also be used on the system volume to ensure application compatibility. NTFS also supports extended-length paths.
- **Security features.** NTFS provides increased data security with features like encryption, rich metadata and disk quotas.
- **Extra storage space.** With NTFS, extra storage space can be created by mounting a volume at any empty folder on a local NTFS volume.


## Advantages of NTFS


- **Support for large volumes.** NTFS supports volumes ranging in size from 16 TB to 8 PB on Windows Server 2019 and newer, and on Windows 10, v1709 and newer.
- **Control.** NTFS provides disc quotas, which enable administrators to limit and control the amount of storage space on shared drives.
- **Performance.** NTFS uses file compression, which shrinks file sizes, increasing file transfer speeds and providing more storage space.
- **Security.** NTFS's built-in security features let administrators grant permissions to sensitive data, restricting access to certain users. NTFS also supports encryption to protect data integrity.
- **Easy logging for transaction rollbacks.** NTFS logs all transactions, making it possible to rollback transactions in order to restore a system and recover data. The built-in logging and auditing system also allows administrators to track files that have been deleted, added or changed in any way.
- **Reliability.** Data and files can be quickly restored in the event of a system failure or error, because NTFS dynamically remaps clusters with bad sectors and allocates new clusters for data.

## Disadvantages of NTFS

The main disadvantages of the NTFS file system are:

- **Limited OS compatibility.** The main disadvantage of NTFS is that it is read-only with non-Windows OSes.
- **It's unsuitable for smaller volumes.** NTFS has a lot of space overhead -- 4 megabytes of drive space on a 100-MB partition -- making it unsuitable for volumes smaller than 400 MB. The overhead also makes it impossible to format floppy disks with NTFS.
- **No built-in file encryption.** While NTFS provides data encryption, it doesn't support file encryption. This can allow anyone to view the data stored on an NTFS volume, for example, by using a low-level disk editing utility.
- **Possible partition size limitations.** Underlying hardware limitations might limit the partition size possible with NTFS. The partition table is also limited to a maximum of 2 TB.

## Source: 
https://www.techtarget.com/searchwindowsserver/definition/NTFS