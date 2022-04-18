---
title: "Properties"
chapter: false
weight: 10
pre:
---

## Properties of EFS 

#### Name:
- A name to describe the file system (optional)
- Under 256 characters and limited to letters, numbers, and some special characters

`STEP 6:`  Skip to the bottom of **Create file system** and select **Customize**

`STEP 7:`  Provide a **Name** for the file system

#### Storage Classes for Availability and Durability:
- **Regional**:  stores data redundantly across several Availability Zones
- **One Zone**:  stores data redundantly within one Availability Zone

`STEP 8:`  Leave the radio button as *Regional* for **Availability and durability**.  

#### Automatic Backups:
- Enable to also backup data to the AWS Backup service

`STEP 9:`  Deselect the *Enable automatic backups* checkbox.

#### Performance Mode:
- General Purpose
    - recommended
    - Supports up to 35,000 IOPS
    - the only option for EFS One Zone
    - is the default mode
- Max I/O:
    - supports 500,000+ IOPS
    - has higher per-operation latencies
- Cannot change the performance mode once it is created

#### Throughput Mode:
- Bursting
    - throughput scales with file system size
    - for traditional applications that have a bursty throughput pattern
    - is the default mode
- Provisioned
    - throughput fixed at specified amount
    - for applications that have a relatively constant throughput

`STEP 10:`  Leave the existing **Performance mode** and **Throughput mode** as is.

#### Encyption:
- Protect EFS data by encrypting it via:
    - Amazon EFS-managed keys *(aws/elasticfilesystem)*, which is the default
    - custom Keys stored in AWS Key Management Service
- Enable encryption of data at rest when creating an Amazon EFS file system
- Enable encryption of data in transit when mounting the file system

`STEP 11:`  Leave the *Enable encryption of data at rest* checkbox selected.

#### Tags:
- Define tags to categorize your bucket for discovery, analysis, and/or cost tracking
- Some labeling examples include:  by project, by owner, by application, by environment, by sensitivity
- Uses key-value pairs

`STEP 12:`  Skip to the bottom of the page and select **Next**.

`STEP 13:`  Leave the **Network** section as-is and select **Next**.

`STEP 14:`  Leave the **File system policy** section as-is and select **Next**.

`STEP 15:`  Skip to the bottom of the page and select **Create**.
