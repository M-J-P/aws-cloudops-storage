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
    - Virtual Hosted Style:
        - General:  https://bucket-name.s3.Region.amazonaws.com/key-name  
	- Example:  https://my-bucket.s3.us-west-2.amazonaws.com/puppy.png
    - Path Style (to be deprecated):
        - General:  https://s3.Region.amazonaws.com/bucket-name/key-name  
	- Example:  https://my-bucket.s3.us-west-2.amazonaws.com/puppy.png
    - S3 Style (via some S3 services)
        - General:  S3://bucket-name/key-name
	- Example:  S3://mybucket/puppy.jpg
- Service quota defaults:
    - 100 buckets per account  
    - no limit to objects within a bucket
       
##### **Object**: a file and any metadata that describes the file
- Has a **Key**
    - The name assigned to an object
    - Used to retrieve the object
- Has a **Version ID**
    - uniquely identifies an object along with the **Key**
    - a string that Amazon S3 generates when you add an object to a bucket
- Has a **Value**
    - The content being stored (e.g. .txt, .csv, .parquet, .png, .mp3)
    - Any any sequence of bytes
    - range zero to 5 TB

##### **Folders**
- are logical only and don't really exist
	- Example:  https://my-bucket.s3.us-west-2.amazonaws.com/animals/dogs/puppy.png
	- */animals/dogs* is a logical folder
	- */animals/dogs/puppy.png* is the **Object**
- can be used as a prefix for S3 **Events**

##### **Metadata**: a set of name-value pairs used to store information regarding the object
- user-defined metadata by customers
- system-metadata by AWS
