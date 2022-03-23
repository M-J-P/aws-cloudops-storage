---
title: "General Properties"
chapter: false
weight: 10
pre:
---

## General Properties of an S3 Bucket

#### Configuration:
1. A unique name to describe the bucket
2. A region in which the bucket is to be created *(e.g. `us-east-1`)*

#### Object Ownership:
1. ACL Disabled *(recommended)*:  ensures that every object in the bucket is owned by the account owner
2. ACL Enabled:  allows for other accounts to own an object that they write to this bucket

#### Public Access:
1. Buckets are private by default, where objects can only be accessed within the account
2. To make objects public, disable the default and select any additional protections
3. Specifically acknowledge if a bucket is to have a public configuration

#### Versioning:
1. Allows for keeping multiple variants of an object in the same bucket
2. Used to preserve, retrieve, and restore every version of every object stored in your Amazon S3 bucket
3. Versioning is often required for additional bucket capabilities *(e.g. Life Cycle Policies, Backups)*

#### Tags:
1. Define tags to categorize your bucket for discovery, analysis, and/or cost tracking
2. Some labeling examples include:  by project, by owner, by application, by environment, by sensitivity
3. Uses key-value pairs

#### Encyption:
1. Protect your objects by encrypting them via:
    1. Amazon S3-managed keys *(SSE-S3)*
    2. Keys stored in AWS Key Management Service *(SSE-KMS)*

#### Object Lock:
1. Store objects using a write-once-read-many *(WORM)* model
2. Pevent objects from being deleted or overwritten for a fixed amount of time or indefinitely
3. Define retention periods through a bucket policy
