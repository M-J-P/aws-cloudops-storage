---
title: "Elastic File System"
chapter: true
weight: 40
pre: "<b>3. </b>"
---

# Elastic File System

## Amazon EFS Defined  

- Amazon EFS is a network file system *(NFS)* used to allow multiple clients to have access to the same set of files.  Key features include:
    - shared file storage:  both Amazon EC2 instances and on-premises servers can simultaneously access a shared Amazon EFS
    - dynamic elasticity:  scales storage capacity up or down
    - scalable performance:  throughput and IOPS *(input/output operations per second)* scale as a file system grows and can burst for short periods
    - fully managed:  AWS manages the file storage infrastructure, removing the complexity of deploying, patching, and maintaining the underpinnings of a file system

## Core Components  

##### **Clients:**
- Amazon EC2s
- on-premises servers
- other machines

##### **Remote Procedure Calls (RPCs):**
- route requests between clients and servers

##### **Mount Target:**
- provides an IP address for an NFSv4 endpoint at which you can mount Amazon EFS

##### **File System:**
- where and how files are stored
- separates data into individual pieces
- has access controls through permissions
- **ADD PICTURE FROM HERE:  https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html**
