---
title: "EBS"
chapter: true
weight: 35
pre: "<b>3. </b>"
---

# Elastic Block Storage

## Amazon EBS Defined  

- Provides block level storage volumes 
- Raw, unformatted block devices. 
- Can mount to EC2 instances.
    - unattached volumes persist independently from the EC2 instance. You can create a file system on top of these volumes, or use them in any way you would use a block device (such as a hard drive). You can dynamically change the configuration of a volume attached to an instance.
- Benefits:
    - quickly accessible data
    - long-term persistence
    - pay for only what is used
- Use cases:
    - storage for file systems
    - storage for databases, 
    - storage for any applications that require fine granular updates and access to raw, unformatted, block-level storage

<img src='/images/block-storage.png' width='1000px'>

## Volume vs. Instance Store vs. Snapshot

- An **EBS Volume** is the underlying disk behind EC2
    - long-term persistence
    - can be unmounted and remounted from EC2s
    - replicated within its availability zone, providing high availability and durability
    - can create a snapshot from it
    - faster launch time
    - can only be encrypted at creation
- An **Instance Store** is ephemeral storage that provides temporary block level storage for an EC2 instance
    - fastest access to data
    - accesses storage from disks that are physically attached to the host computer
    - if an instance is stopped or terminated, any data on instance store volumes is lost; a reboot still persists the data
- A **Snapshot** is a point in time backup of specific volume
    - can be encrypted at anytime
