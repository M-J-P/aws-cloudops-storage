---
title: "Storage Classes"
chapter: false
weight: 10
pre: 
---

## Overview

- Each **Object** in Amazon S3 has a storage class associated with it
- The console shows the storage class for all the objects in the bucket list 
- The class is dependent on the use case and performance access requirements; factors are:
    - availability
    - retention
    - cost
- Each class offers high durability - 99.999999999% *(11 9's)*

## Durability versus Availability 

- **Durabilty** - the percentage that an object will not be lost. For example, the S3 Standard Tier is designed for 99.999999999% durability. This means that if you store 100 billion objects in S3, you will lose one object at most.
- **Availability** - the percentage of time that a workload is available for use. 

## S3 Storage Class Types

<img src='/images/s3-storage-classes-2021.png' width='1600px'>

- **S3 Intelligent-Tiering**
    - for unknown or changing access
    - automatic cost savings for data with unknown or changing access patterns
    - small monthly charge
- **S3 Standard**
    - for frequently accessed data
    - resilient against events that impact an entire Availability Zone
    - 99.99% availability *(4 9's)*
- **S3 Standard-IA**
    - for less frequently accessed data
    - saves up to 40% on storage costs
    - 99.9% availability *(3 9's)*
    - for objects larger than 128 KB (charged for 128 KB if less)
    - minimum retention of at least 30 day *(charged for 30 days if deleted earlier)*
- **S3 One Zone-IA**
    - for infrequently accessed data stored only in one Availability Zone
    - costs 20% less than S3 Standard-IA
    - 99.5% availability
    - for objects larger than 128 KB (charged for 128 KB if less)
    - minimum retention of at least 30 day *(charged for 30 days if deleted earlier)*
- **Glacier Instant Retrieval**
    - for long-lived data that is accessed once per quarter and requires millisecond retrieval
    - up to 68% lower cost than S3 Standard-IA
    - immediate retreival
    - 99.9% availability *(3 9's)*
- **Glacier Flexible Retrieval** *(f.k.a. Glacier)*
    - for archive data that is accessed 1-2 times per year and is retrieved asynchronously
    - up to 10% lower cost than Glacier Instant Retrieval
    - retrieval options of:
        - Expedited *(1-5 minutes)*
        - Standard *(3-5 hours)*
        - Bulk *(5-12 hours)*
    - 99.99% availability *(4 9's)*
    - free bulk retrievals
    - use cases:
        - backup
        - disaster recovery
        - offsite data storage need
- **Glacier Deep Archive**
    - long-lived archive data that is accessed less than once per year and is retrieved asynchronously
    - up to 75% lower cost than Glacier Flexible Retrieval
    - retrieval options of:
        - Standard *(up to 12 hours)*
        - Bulk *(up to 24 hours)*
    - 99.99% availability *(4 9's)*
- **S3 Outposts**
    - for on-premises data
