---
title: "Storage Gateway Options"
chapter: false
weight: 10
pre:
---

## Overview

- Storage Gateways have three options, where two of these have sub-options

## File Gateways

##### **Amazon S3 File Gateway**

<img src='/images/file-gateway.png' width='800px'>

- Stores and retrieves **objects in Amazon S3**
    - The gateway asynchronously updates the objects in Amazon S3 as files change
    - The key becomes the path
    - Objects are encrypted with Amazon S3–server-side encryption keys (SSE-S3)
- Uses industry-standard file protocols:
    - Network File System (**NFS**) for Linux based
    - Server Message Block (**SMB**) for Windows based
- Connect through:
    - Connect Direct
    - HTTPS
    - Amazon VPC
- Optimizes data transfer using multipart parallel uploads or byte-range downloads
- Local cache is maintained
    - Provides low latency access to the recently accessed data
    - Reduces data egress charges

##### **Amazon FSx File Gateway**
- Stores and retrieves **objects in Amazon FSx Windows Server**
    - Local file writes and reads benefiting from all the features available on FSx for Windows File Server
    - 1:1 correspondence between the remote and locally visible files
- Joins with the on-premises **Microsoft Active Directory domain**
- Connect through:
    - Connect Direct
    - VPN
    - Amazon VPC

## Volume Gateways

<img src='/images/volume-gateway.png' width='800px'>

- Provides an **iSCSI** (Internet Small Computer System Interface) target, which enables you to create **block storage volumes**
- Deployed into your on-premises environment as a VM


##### **Cached Volume**
- Stores data Amazon S3
- Retains a **local copy of frequently accessed data subsets**
- Offers substantial cost savings on primary storage
- Minimizes the need to scale on-premises storage
- Size ranges from 1 GiB to 32 TiB

##### **Stored Volume**
- Backs up point-in-time snapshots on Amazon S3
- Retains a **local copy of the entire dataset**, enabling low-latency access
- Provides durable and inexpensive offsite backups
- Size ranges from 1 GiB to 16 TiB

## Tape Gateway

<img src='/images/tape-gateway.png' width='800px'>

- Provides cloud-backed **virtual tape storage**
- Deployed into your on-premises environment as a VM

##### **Tape Gateway**
- Cost-effectively and durably archive backup data via:
    - S3 Glacier Flexible Retrieval
    - S3 Glacier Deep Archive
- Scales seamlessly
- Core components:
    - Virtual tape:  is like a physical tape cartridge but is stored in the AWS Cloud.
        - Can be blank
        - Can have data
        - Size ranges from 100 GiB and 5 TiB.
        - 1,500 tapes per gateway
    - **Virtual tape library (VTL)**: is like a physical tape library available on-premises with robotic arms and tape drives
        - Includes the collection of stored virtual tapes
	- Each Tape Gateway comes with one VTL
        - Created virtual tapes appear in VTL
        - Tapes in the VTL are backed up by Amazon S3
    - Archive:  is analogous to an offsite tape holding facility
