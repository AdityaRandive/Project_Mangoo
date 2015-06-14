# Project_Mangoo
Thread Consistent File Storage in Databases (Bachelor Thesis Project)

### Abstract
File system in User space (FUSE) is an operating system mechanism for Unix-like computer operating systems. FUSE is a means of providing an interface with code that doesn't run in the kernel. This can dramatically improve stability and security, since kernel code is privileged, while userspace code isn't. Mangoo is a flexible framework for storage. Applications can use Mangoo to use different functionalities, such as use of databases, to store their data. Mangoo uses the Mangoo data stores to achieve these functionalities. Mangoo framework offers two interfaces - one to applications and the other to file stores. Mangoo serves as a connection between the two. For example
Mangoo-Fuse front-end (Mangoo-Fuse) and Berkeley-DB backend (DBFS) together enable applications to use Berkeley-DB to store files.
The principal objectives aimed to be achieved are:
  - Support for multiple threads in Mangoo.
  - Implement Berkeley-DB transactions in Mangoo.
  - To address the issue of Multiple Read/Write by Concurrent processes which leads to inconsistency in the database.
  - To apply this at the System/Database level.
  - To create a locking mechanism for the same.
Support for multiple threads will enable more efficient use of system to make processing faster
and concurrent. Support for Transactions in DBFS aims to prevent unpredictable and inconsistent
results caused by conflicts between two threads accessing same database elements simultaneously.
We can achieve this by adding our own functionality to the Mangoo framework which will enable
the use of multiple threads to achieve the concurrent write scenario. We could also add Transac-
tion support modules(read/write/open) which will prevent inconsistency and unpredictable results
caused by conflicts between two threads accessing same database elements simultaneously thus
maintaining a thread consistent database which will abide by the ACID/BASE properties.
