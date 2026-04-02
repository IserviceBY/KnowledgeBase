---
lastSync: Mon Mar 23 2026 12:29:59 GMT+0300 (Moscow Standard Time)
---
**FAT overview**

FAT is by far the most simplistic of the file systems supported by Windows NT. The FAT file system is characterized by the file allocation table (FAT), which is really a table that resides at the very "top" of the volume. To protect the volume, two copies of the FAT are kept in case one becomes damaged. In addition, the FAT tables and the root directory must be stored in a fixed location so that the system's boot files can be correctly located.

A disk formatted with FAT is allocated in clusters, whose size is determined by the size of the volume. When a file is created, an entry is created in the directory and the first cluster number containing data is established. This entry in the FAT table either indicates that this is the last cluster of the file, or points to the next cluster.

Updating the FAT table is very important as well as time consuming. If the FAT table is not regularly updated, it can lead to data loss. It is time consuming because the disk read heads must be repositioned to the drive's logical track zero each time the FAT table is updated.

#### FAT type maximum clusters and volume sizes

| **Type** | **Maximum cluster** | **Maximum volume sizes** |
| -------- | ------------------- | ------------------------ |
| FAT12    | 4,078               | 256 MB                   |
| FAT16    | 65,524              | 2 GB                     |
| FAT32    | 268,435,456         | 2 TB                     |

For FAT12 and FAT16, the maximum file size is limited to the maximum volume size. The first implementation of FAT32 had a maximum file size of 2 GB. In 1996, multiple vendors met at a Large File Summit and agreed to a standard addressing scheme for 64 bit numbers, and this raised the FAT32 maximum file size to 4 GB.

Surpassing that limit was one of the main reasons for the design of Extensible FAT (exFAT) file system. This was introduced as part of Windows CE in 2006. In addition to options for larger media and file sizes, exFAT also introduced international character sets, improved time granularity, and other modern features. The exFAT format was adopted by the SD Association for SDXC media in 2009, and is widely used today in cameras, cars, and other digital devices. This allows the removable media to be used in desktop systems and other devices with no confusion.


Source: 
https://www.tuxera.com/technical-articles/understanding-fat-exfat-file-system/