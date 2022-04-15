---
title: "Storage Classes"
chapter: false
weight: 10
pre: 
---

## Overview

- Provides continuous availability to data
- Pay only for the storage used by your file system
- No minimum fee or setup cost
- Throughput options include Bursting and Provisioned
- Each class offers high durability - 99.999999999% *(11 9's)*

## EFS Storage Class Types
- **EFS Standard**
    - Frequently accessed data
    - Stored redundantly across Availability Zones within a Region
    - Lowest latency
    - 99.99% availability *(4 9's)*
    
- **EFS Standard - Infrequently Accessed**
    - Reduces storage costs for files that are not accessed every day
    - Stored redundantly across Availability Zones within a Region
    - Higher first byte latency
    - 99.99% availability *(4 9's)*

- **EFS One Zone**
    - Frequently accessed data
    - Stored redundantly within one Availability Zone
    - Lowest latency
    - 99.90% availability *(3 9's)*

- **EFS One Zone - Infrequently Accessed**
    - Reduces storage costs for files that are not accessed every day
    - Stored redundantly within one Availability Zone
    - Higher first byte latency
    - 99.90% availability *(3 9's)*
