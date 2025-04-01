---
title: "S3"
chapter: true
weight: 20
pre: "<b>1. </b>"
---

# Simple Storage Service

## Amazon S3 Defined

- Amazon Simple Storage Service is an object storage service that offers:
    - scalability
    - data availability
    - security
    - performance
- Use cases include:
    - data lakes
    - websites
    - mobile applications
    - backup and restore
    - archive
    - enterprise applications
    - IoT devices
    - big data analytics

## S3 Bucket Types

##### **General Purpose Bucket**: the standard, versatile container for storing objects 
- This course will cover this type of bucket
- Other available options include:

##### **Directory Buckets**: organize data hierarchically into directories
- Its implementation uses S3 Express One Zone
- Designed for ultra-low latency and high throughput
- Use cases include applications that require very fast access to data, such as data analytics, machine learning, and high-performance computing
- Generally available at the end of 2023

##### **Table Buckets**: optimized for storing and managing tabular data
- Offers built-in support for Apache Iceberg, a popular open-source table format
- Currently in preview release, available in early-stage in three US regions as of 2025

## Core Components

##### **Bucket**: a container for objects
- Has a globally unique name
    - **Virtual Hosted Style**:
        - general:  https://bucket-name.s3.Region.amazonaws.com/key-name
        - example:  https://my-bucket.s3.us-west-2.amazonaws.com/puppy.png
    - **Path Style** (was to be deprecated but still supported):
        - general:  https://s3.Region.amazonaws.com/bucket-name/key-name
        - example:  https://s3.us-west-2.amazonaws.com/my-bucket/puppy.png
    - **S3 Style** (via some S3 services)
        - general:  S3://bucket-name/key-name
        - example:  S3://mybucket/puppy.jpg
- Service quota defaults:
    - 10,000 buckets per account (up to 1 million buckets)
    - no limit to objects within a bucket

##### **Object**: a file and any metadata that describes the file
- Has a **Key**
    - the name assigned to an object
    - used to retrieve the object
- Has a **Value**
    - the content being stored (e.g. .txt, .csv, .parquet, .png, .mp3)
    - any sequence of bytes
    - ranges from zero to 5 TB
- Has a **Version ID** (if versioning is enabled)
    - uniquely identifies an object along with the **Key**
    - a string that Amazon S3 generates when you add an object to a bucket

##### **Folders**
- Are logical only and don't really exist
    - example:  https://my-bucket.s3.us-west-2.amazonaws.com/animals/dogs/puppy.png
        - *animals* is a logical folder
        - *dogs* is a logical folder
        - */animals/dogs/puppy.png* is the **Key**

##### **Prefixes**
- Are strings preceding the object name
    - example:  https://my-bucket.s3.us-west-2.amazonaws.com/animals/dogs/puppy.png
        - */animals* is a prefix
        - */animals/dogs* is a prefix
- Are used to improve performance by creating partitions
- Can be used as part of S3 **Events**

##### **Metadata**: a set of name-value pairs used to store information regarding the object
- System-metadata by AWS
    - Examples:
        - Content-Length
        - Content-Type
        - Last-Modified
        - x-amz-storage-class
        - x-amz-server-side-encryption
- User-defined metadata by customers
