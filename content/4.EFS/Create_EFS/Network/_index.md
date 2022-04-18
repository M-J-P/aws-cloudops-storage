---
title: "Network"
chapter: false
weight: 30
pre:
---

## Defining the Network and Permissions

#### Virtual Private Cloud *(VPC)*:
1. Select the VPC to which the EC2 instances will connect
2. Under 256 characters and limited to letters, numbers, and some special characters

#### Mount Targets
1. An NFSv4 endpoint at which you can mount an Amazon EFS file system
2. One per Availability Zone *(recommended)*
    - Availability Zone
    - Subnet ID
    - IP Address
    - Security Groups

#### Permissions:
1. Select a common policy or define a custom one.  Common include:
    - Prevent root access by default
    - Enforce read-only access by default
    - Prevent anonymous access
    - Enforce in-transit encryption for all clients
