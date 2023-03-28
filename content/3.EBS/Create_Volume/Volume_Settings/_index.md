---
title: "Volume Settings"
chapter: false
weight: 10
pre:
---

## General Settings of an EBS Volume

#### Volume Type:
- Select the type of the bucket to best align with the use case

`STEP 6:`  Select **General Purpose SSD (gp-3)** from the drop-down.

#### Size (GiB):
- Configure how large the volume is:
    - General Purpose SSD - 1 GiB (min) and 16 TiB (max)
    - Provisioned IOPS SSD - 4 GiB (min) and 16 TiB (max)
    - Throughput Optimized HDD - 125 GiB (min) and 16 TiB (max)
    - Cold HDD - 125 GiB (min) and 16 TiB (max)
    - Magnetic - 1 GiB (min) and 1 TiB (max)

`STEP 7:`  Enter the minimum size of **1 GiB**.  *(feel free to experiment with numbers)*

#### IOPS:
- The count of the read/write operations per second  
- Configure the requested number of I/O operations per second
    - General Purpose SSD (gp2) - 100 to 16,000 IOPS (proportionate to the size)
    - General Purpose SSD (gp3) - 3,000 to 16,000 IOPS
    - Provisioned IOPS SSD - 100 to 64,000 IOPS
    - Throughput Optimized HDD - performance is measured in throughput (MiB/s)
    - Cold HDD - performance is measured in throughput (MiB/s)
    - Magnetic - 100 IOPS on average; burstable

`STEP 8:`  Enter the minimum size of **3000 IOPS**.  *(feel free to experiment with numbers)*

#### Throughput: 
- The measurement of read/write bits per second that are transferred over a network  
- Configure the throughput performance that the volume can support, measured in MiB/s.
    - General Purpose SSD (gp2) - not applicable
    - General Purpose SSD (gp3) - 125 MiB/s (min) to 1000 MiB/s (max)
    - Provisioned IOPS SSD - not applicable
    - Throughput Optimized HDD - 40 MiB/s per TiB (proportionate to the size)
    - Cold HDD - 12 MiB/s per TiB (proportionate to the size)
    - Magnetic - not applicable

`STEP 9:`  Enter the minimum throughput of **125**.

#### Availability Zone:
- The AZ in which to create the volume
- Can only be attached to instances that are in the same AZ

`STEP 10:`  Select **us-east-1a** from the drop-down.

#### Snapshot ID:
- The ability to create a volume from a point-in-time snapshot

`STEP 11:`  Select *Don't create volume from a snapshot* from the drop-down.

#### Encryption:

`STEP 12:`  Select the *Encrypt this volume* checkbox.

#### Tags:
- Additional labels using key/value pairs.

`STEP 13:`  Select **Add tag** and enter the following ...
- **Key** ==> *EBS-Backup-Daily*
- **Value** ==> *TRUE*

`STEP 14:`  Skip to the bottom and select **Create volume**.
<br>
<br>
<br>
`BONUS:`  Create a volume for each EBS type.  Notice the differences with input options and ranges.  *(be sure to remove them once done)*
