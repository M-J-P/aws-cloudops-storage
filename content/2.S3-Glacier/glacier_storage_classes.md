---
title: "Storage Classes"
chapter: false
weight: 10
pre: 
---

## Overview

- Purpose-built for data archiving
- Provides high performance
- Offers retrieval flexibility
- Lowest cost archive storage in the cloud
- Unlimited scalability
- Each class offers high durability - 99.999999999% *(11 9's)*

## Glacier Storage Class Types
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

<img src='/images/s3-storage-classes-2021.png' width='1600px'>

*from Re:Invent 2021*


