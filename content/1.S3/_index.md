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

## Core Components  

##### **Bucket**: a container for objects  
- Has a globally unique name  
    - **Virtual Hosted Style**:
        - general:  https://bucket-name.s3.Region.amazonaws.com/key-name  
	- example:  https://my-bucket.s3.us-west-2.amazonaws.com/puppy.png
    - **Path Style** (to be deprecated):
        - general:  https://s3.Region.amazonaws.com/bucket-name/key-name  
	- example:  https://my-bucket.s3.us-west-2.amazonaws.com/puppy.png
    - **S3 Style** (via some S3 services)
        - general:  S3://bucket-name/key-name
	- example:  S3://mybucket/puppy.jpg
- Service quota defaults:
    - 100 buckets per account  
    - no limit to objects within a bucket
       
##### **Object**: a file and any metadata that describes the file
- Has a **Key**
    - the name assigned to an object
    - used to retrieve the object
- Has a **Version ID**
    - uniquely identifies an object along with the **Key**
    - a string that Amazon S3 generates when you add an object to a bucket
- Has a **Value**
    - the content being stored (e.g. .txt, .csv, .parquet, .png, .mp3)
    - any sequence of bytes
    - ranges from zero to 5 TB

##### **Folders**
- Are logical only and don't really exist
	- example:  https://my-bucket.s3.us-west-2.amazonaws.com/animals/dogs/puppy.png
	- */animals/dogs* is a logical folder
	- */animals/dogs/puppy.png* is the **Object**
- Can be used as a prefix for S3 **Events**

##### **Metadata**: a set of name-value pairs used to store information regarding the object
- User-defined metadata by customers
- System-metadata by AWS
