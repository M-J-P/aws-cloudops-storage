---
title: "Volume Types"
chapter: false
weight: 10
pre: 
---

## EBS Volume Types

- **General Purpose Solid State Drive (SSD) volumes (gp2 and gp3)**
    - balance price and performance
    - support a wide variety of transactional workloads
    - Use cases:
        - boot volumes
	- medium-size single instance databases
	- development and test environments
- **Provisioned IOPS SSD volumes (io1 and io2)**
    - meet the needs of I/O-intensive workloads
    - provide a consistent IOPS rate
    - provide the highest levels of volume durability.
    - most expensive
    - Use cases:
        - mission-critical applications
	- large database workloads such as MongoDB, Microsoft SQL Server, Cassandra, Oracle, MySQL, and PostgreSQL
- **Throughput Optimized HDD volumes (st1)**
    - provide low-cost magnetic storage
    - performance in terms of throughput rather than IOPS
    - Use cases:
        - large, sequential workloads
	    - Amazon EMR
	    - ETL (extract-transform-load)
	    - data warehousing
	    - data streaming
	    - log processing
- **Cold HDD volumes (sc1)**
    - provide low-cost magnetic storage
    - performance in terms of throughput rather than IOPS
    - least expensive
    - Uses cases:
        - storage for infrequently accessed data
        - sequenital workloads

- **Magnetic volumes (standard)**
    - previous generation storage
    - Uses cases:
        - storage for infrequently accessed data
        - less demanding workloads

<img src='/images/ebs-volume-types.png' width='1000px'>

## Drive Acroynms
- SSD = Solid State Drive
- HDD = Hard Disk Drive
