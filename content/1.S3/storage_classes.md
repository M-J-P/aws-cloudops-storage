---
title: "Storage Classes"
chapter: false
weight: 10
pre: 
---

## Description

- Each **Object** in Amazon S3 has a storage class associated with it
- The console shows the storage class for all the objects in the list 
- The class is dependent on the use case and performance access requirements
- Each class offers high durability - 99.999999999% *(11 9's)*

## Durability versus Availability 

- **Durabilty** - the percentage that an object will not be lost. For example, the S3 Standard Tier is designed for 99.999999999% durability. This means that if you store 100 billion objects in S3, you will lose one object at most.
- **Availability** - the percentage of time that a workload is available for use. 

## S3 Storage Class Types
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
- **S3 One Zone-IA**
    - for infrequently accessed data stored only in one Availability Zone
    - costs 20% less than S3 Standard-IA
    - 99.5% availability
- **S3 Glacier**
    - for archive data
- **S3 Outposts**
    - for on-premises data

<img src='/images/s3-storage-classes-2021.png' width='1600px'>

*from Re:Invent 2021*


