---
title: "Properties"
chapter: false
weight: 10
pre:
---

## Properties of EFS 

#### Name:
1. A name to describe the file system (optional)
2. Under 256 characters and limited to letters, numbers, and some special characters

#### Storage Classes for Availability and Durability:
1. Regional:  stores data redundantly across several Availability Zones
2. One Zone:  stores data redundantly within one Availability Zone

#### Automatic Backups:
1. Enable to also backup data to the AWS Backup service

#### Performance Mode:
1. General Purpose
    - Recommended
    - supports up to 35,000 IOPS
    - The only option for EFS One Zone
    - Is the default mode
2. Max I/O:
    - supports 500,000+ IOPS
    - has higher per-operation latencies
3. Cannot change the performance mode once it is created

#### Throughput Mode:
1. Bursting
    - Throughput scales with file system size
    - For traditional applications that have a bursty throughput pattern
    - Is the default mode
2. Provisioned
    - Throughput fixed at specified amount
    - For applications that have a relatively constant throughput

#### Encyption:
1. Protect EFS data by encrypting it via:
    - Amazon EFS-managed keys *(aws/elasticfilesystem)*, which is the default
    - Custom Keys stored in AWS Key Management Service
2. Enable encryption of data at rest when creating an Amazon EFS file system
3. Enable encryption of data in transit when mounting the file system

#### Tags:
1. Define tags to categorize your bucket for discovery, analysis, and/or cost tracking
2. Some labeling examples include:  by project, by owner, by application, by environment, by sensitivity
3. Uses key-value pairs
