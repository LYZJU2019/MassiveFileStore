# DSFS
A distributed file system for massive small files written in Java


## Motivation

FastDFS, which is written in C programming language, is an existing system realizing similar functionalities. However, the shortcomings are:

- Slow maintanance and activeless community
- Lots of Bugs
- Almost impossible to view the source code to get the idea of how it works behind

Small companies tends to store their files on third-party clouds. But copywrite issue emerges. 

To store a large number of sensitive files, it better to develop their own remote file systems to suit the bussiness need for small companies.

## Architecture

## Building Instructions


## Building Pieces

- [x] Master-Slave Architecture. DataNodes & NameNodes
- [x] Google RPC framework to enable DataNode registration and HeartBeat from DataNode, common file operations (`mkdir`, `open`, `write`, etc.) from FS clients
- [x] EditLog (Double buffer implementation) to record file operations in memory from all clients, avoiding frequent write to disk files
- [x] fsimage Checkpoint to compress previous editlogs, accelerating reboot speed of NameNode

## Performance

## Developer Logs

- 2023.6.2 Project start, get initial Java code running.
- 2023.6.4 DataNodes can send registration and heartbeat requests to central NameNode and get corresponding responses.
- 2023.6.5 Implemented the Recovery mechanism on NameNode for DataNode crashes.
- 2023.6.8 Finished the in-memory INode directory structure (the file system namespace) on NameNode.
- 2023.6.10 Double buffer for EditLog
- 2023.6.13 Fixed the sync issues when massive threads writing into editlog buffer and sync to disks when the buffer is full.
- 2023.6.14 - 18 Performance test stage 1
  
