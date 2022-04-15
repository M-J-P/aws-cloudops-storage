---
title: "AWS Backup"
chapter: true
weight: 70
pre: "<b>6. </b>"
---

# AWS Backup

## AWS Backup Defined  

- A centralized service that manages and automates backups across other AWS services
- Protects storage volumes, databases, and file systems
- Consolidated view for monitoring, logging, and alerts
- Define schedules for automated backups
- Configure retention management and lifecycle management
- Apply unique backup policies using tags
- Encrypts data in transit and at rest
- Monitor backup and restore activities
- Cross-account management with AWS Organizations
- Efficiently stores your periodic backups incrementally
    - first backup is a full copy of the data
    - saves storage costs

## Supported data services
- Aurora
- DocumentDB
- DynamoDB
- EBS
- EFS
- FSx for Lustre
- FSx for Windows File Server
- Neptune
- RDS
- S3
- Storage Gateway

## Core Components  

##### **Vault**: a container that stores and organizes backups
- A logical construct that lives within the account
- Behind the curtain, backups are stored on S3 across AWS owned accounts in the same region
- Protected by AWS KMS encryption key
- Backups cannot be re-encrypted (ransomeware protection)
- Provides operational risk protection
- Provides cyber threat actor protection
- Access policies:
    - grant access to users to create backup plans and on-demand backups
    - limit ability to delete recovery points once created.
- Vault Lock:
    - prevent delete operations
    - prevent updates that may alter/shorten their retention period
       
##### **Plan**: defines when and how to back up AWS resources
- Assign resources to backup plans
- Define the backup frequency
    - hourly
    - 12 hours
    - daily
    - weekly
    - monthly
    - custom period using CRON expression (minimum of hourly)
- Enable continuous backups checkbox to create a point-in-time restore (PITR)-enabled continuous backup rule
    - RDS
    - S3
- Set the backup window
- Enable replication to other regions
- Define the retention period
