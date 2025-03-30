---
title: "File Server (FSx)"
chapter: true
weight: 50
pre: "<b>5. </b>"
---

# File Server (FSx)

## Amazon FSx Defined  

- Amazon FSx provides file servers with storage volumes, hardware updates, software configuration, and backups that are fully managed and automated
    - Fast:  delivers sustained high read and write speeds and consistent low latency data access
    - Available and Durable:  choose single-AZ or multi-AZ deployment typesn; choose from scratch or persistent storage
    - Inexpensive:  multiple deployment options where customers only pay for resources consumed
    - Secure and Compliant:  automatically encrypts your data at-rest and in-transit; complies with ISO, PCI-DSS, and SOC certifications, and is HIPAA eligible
    - Integration with AWS services:  user other AWS services to process and manage data  
- Four FSx types, ordered by release date:
    - Windows File Server
    - Lustre
    - NetApp ONTAP
    - OpenZFS


## Amazon EFS versus FSx

- EFS: This is a standard network filesystem (NFS)
- FSx for Windows: Service Message Block (SMB) / Common Internet File System (CIFS) fileshare as a service for Windows nodes
- FSx for Lustre: High performance shared filesystem for high performance computing (HPC) workloads
- FSx for ONTAP: a filesystm if for use with NetApp
- FSx for OpenZFS: a filesystem for use with Zettabyte File System (ZFS)
