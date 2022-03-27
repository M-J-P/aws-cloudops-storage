---
title: "S3 Glacier"
chapter: true
weight: 30
pre: "<b>2. </b>"
---

# S3 Glacier

## S3 Glacier Defined  

- An extremely low-cost storage service that provides:
    - flexible storage
    - security
    - durability
    - backup
    - archival
- Use cases include:
    - media asset workflows
    - healthcare information archiving
    - regulatory, compliance, and business policy archiving
    - scientific data storage
    - digital preservation
    - long-term backup retention
    - on-premises tape replacement

## Core Components  

##### **Vault**: a container for storing archives 
- Service quota defaults:
    - 1000 vaults per AWS account per region

##### **Archives**: what is stored in the Vault
- Archives can be:
    - single objects 
    - a collection of objects *(e.g. TAR or ZIP)*
- Maximum of 40 TB
