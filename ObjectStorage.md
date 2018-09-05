# Basics
Before stepping into the concept of object storage we should know about that `what
are the limitation in other type of storage so that object storage come into the play ?`
Let's take example of block storage
### what is block storage ?
Block storage devices provide fixed-sized raw storage capacity. Each storage volume can be treated as an independent disk drive and controlled by an external server operating system.</br>
File system like FAT32, NTFS, EXT3, and EXT4.
* #### Use Case
   * Block storage is ideal for databases, since a DB requires consistent I/O performance and low-latency connectivity.

   * You can use block storage for (RAID) Volumes, where you combine multiple disks organized    through stripping or mirroring.

   * Any application which requires service side processing, like Java, PHP, and .Net will require block storage.

# Introduction
Block storage volumes can only be accessed when they’re attached to an operating system. But data kept on object storage devices, which consist of the object data and metadata, can be accessed directly through APIs or http/https. You can store any kind of data, photos, videos, and log files. The object store  guarantees that the data will not be lost. Object storage data can be replicated across different data centers and offer simple web services interfaces for access.

* ### Use Case
  * Storage of unstructured data like music, image, and video files.
  * Storage for backup files database dumps, and log files.
  * Large data sets. Whether you’re storing pharmaceutical or financial data, or multimedia files such as photos and videos, storage can be used as your big data object store.
  * Archive files in place of local tape drives. Media assets such as video footage can be stored in object storage and archived to AWS glacier.<br>

Object storage, by contrast, doesn’t split files up into raw blocks of data. Instead, entire clumps of data are stored in, yes, an object that contains the data, metadata, and the unique identifier. There is no limit on the type or amount of metadata, which makes object storage powerful and customizable.

Companies like Amazon (with S3) provide object storage via its public cloud platform at massive scale, while object storage can be implemented in the company data center using technology like OpenStack’s Swift or EMC’s Atmos.
