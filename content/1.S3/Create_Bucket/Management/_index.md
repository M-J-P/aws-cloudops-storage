---
title: "Management"
chapter: false
weight: 40
pre:
---

## Management of an S3 Bucket

#### Lifecycle Rules:
1. Manage objects throughout their lifecycle so that they are stored cost effectively.
2. A set of rules that define actions:
    - transition actions:  move objects to a less expensive storage class after a certain period of time
    - expiration actions:  delete objects after a certain period of time
3. Filter objects to be transitioned by:
    - prefix
    - tags
    - size

#### Replication Rules:
1. Enables automatic, asynchronous copying of objects across Amazon S3 buckets
    - Same-Region Replication (SRR)
    - Cross-Region Replication (CRR)
2. To a single destination bucket or to multiple destination buckets
3. Replicate all objects or designate a filter
    - filter by prefix
    - filter by tag
4. Preserve encryption if desired
5. Uses cases:
    - Replicate objects while retaining metadata
    - Replicate objects into different storage classes
    - Maintain object copies under different ownership
    - Keep objects stored over multiple AWS Regions
