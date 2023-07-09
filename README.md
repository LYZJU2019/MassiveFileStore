# DSFS
A distributed file system for massive small files written in Java


## Motivation

FastDFS, which is written in C programming language, is an existing system realizing similar functionalities. However, the shortcomings are:

- Slow maintanance and activeless community
- Lots of Bugs
- Almost impossible to view the source code to get the idea of how it works behind

Small companies tends to store their files on third-party clouds. But copywrite issue emerges. 

To store a large number of sensitive files, it better to develop their own remote file systems to suit the bussiness need for small companies.


## Building Pieces

- [x] Master-Slave Architecture. DataNodes & NameNodes
- [x] Google RPC framework to enable DataNode registration & HeartBeat
- [x] editlog to avoid frequent write request to disk files, fsimage Checkpoint to accelerate reboot speed of NameNode
