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
