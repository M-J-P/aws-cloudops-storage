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
- Not encrypted by default; however this configuration can be changed
- Cannot encrypt if initially created as unencrypted
- Benefits:
    - quickly accessible data
    - long-term persistence
    - pay for only what is used
- Use cases:
    - storage for file systems
    - storage for databases
    - storage for any applications that require fine granular updates and access to raw, unformatted, block-level storage

<img src='/images/block-storage.png' width='1000px'>

## Root Volume vs. Attached Volume vs. Snapshot

- An **EBS Root Volume** is the underlying disk behind EC2
    - launched from either an instance store-backed AMI or an Amazon EBS-backed AMI (faster)
    - by default, is deleted when the EC2 instance is terminated
    - replicated within its availability zone, providing high availability and durability
    - can be unmounted and remounted from EC2s only after the instance is stopped
    - can create a snapshot from it
    - up to 16 TiB
- An **EBS Attached Volume** is additional disk to provide more storage to an EC2 instance
    - added at the time of EC2 creation or can be added later
    - long-term persistence
    - replicated within its availability zone, providing high availability and durability
    - can be unmounted and remounted from EC2s
    - can create a snapshot from it
    - up to 64 TiB
- A **Snapshot** is a point in time backup of specific volume
    - can be encrypted whilst creating a copy of a non-encrypted snapshot
