---
title: "FSx File Systems"
chapter: false
weight: 10
pre: 
---

## Overview

- Four widely used options
- Choosing the right system is typically driven by:
    - an existing familiarity with a given file system
    - matching the requirements of the workload
        - features
        - performance needs
        - data management capabilities

## FSx Server Types
- **FSx for Windows File Server**
    - Provides fully managed **Microsoft Windows** file servers
    - Fast
        - SSD storage for consistent sub-millisecond latencies
        - up to 3 GB/s of throughput
        - up to hundreds of thousands of IOPS
    - Easily move Windows based applications to AWS
    - Supports code, applications, and tools that Windows developers and administrators use
        - **Server Message Block *(SMB)*** protocol for sharing access to files, printers, serial ports and other resources on a network
        - Windows NTFS *(New Technology File System)*
        - **Microsoft Active Directory *(AD)* integration**
    - Access from Linux, Windows, and macOS compute instances running in AWS or on premises

- **Amazon FSx for Lustre**
    - High performance for these types of workloads:
        - machine learning
        - high performance computing **(HPC)**
        - video processing
        - financial modeling
    - **Fastest**
        - provides sub-millisecond latencies
        - up to hundreds of GBps of throughput
        - up to millions of IOPS
    - **POSIX-compliant** for easy use of Linux-based applications
    - Works with Linux operating system
    - Access from EC2, EKS, and ECS (AWS or on-premises)
    - Integrates seamlessly with S3 and SageMaker

- **Amazon FSx for NetApp ONTAP**
    - Snapshot, clone, replicate, and compress your files with the click of a button
    - Fast
        - SSD storage for consistent sub-millisecond latencies
        - up to 3 GB/s of throughput
        - up to hundreds of thousands of IOPS
    - Automatically tiers your data to lower-cost
    - Integrates Microsoft Active Directory *(AD)*
    - Access from Linux, Windows, and macOS compute instances running in AWS or on premises

- **Amazon FSx for OpenZFS**
    - Easily move data from on-premises ZFS or other Linux-based file servers to AWS
    - Provides OpenZFS data management capabilities including compression, point-in-time snapshots, and cloning
    - Faster
        - SSD storage for consistent microsecond latencies
        - up to 12.5 GB/s of throughput
        - up to one million IOPS
    - Uses **NFS protocol** *(v3, v4.0, v4.1, v4.2)*
    - Access from Linux, Windows, and macOS compute instances running in AWS or on premises
