---
title: "Advanced Properties"
chapter: false
weight: 20
pre:
---

## Advanced Properties of an S3 Bucket

`STEP 16:`  From the Buckets dashboard, notice the **AWS Region** and **Access** for the newly created bucket.

#### **SAMPLES**

<img src='/images/bucket-dashboard.png' width='900px'>

`STEP 17:`  Select the newly created bucket.

`STEP 18:`  Navigate to the **Properties** tab.

#### Intelligent-Tiering Configuration:
- Set optimization for objects that will be rarely accessed for long periods of time

#### Server Access Logging:
- Provides detailed records for the requests that are made to a bucket
- Access log information can be useful in security and access audit
- Learn about your customer base and understand your Amazon S3 bill

#### AWS CloudTrail data events:
- Provides a record of actions *(events)* taken by a user, role, or an AWS service in Amazon S3
- Can enable continuous delivery of CloudTrail events to an Amazon S3 bucket

#### Event Notifications:
- Send a notification message to a destination whenever those events occur:
    - Amazon SNS
    - Amazon SQS
    - Lambda
- General configuration:
    - define an event name
    - use prefix *(e.g. logical folders)*
    - use suffix *(e.g. file extensions)*
- Event types:
    - object created
    - object removed
    - object restored
    - lifecycle
    - others
- Amazon EventBridge *(f.k.a. Amazon CloudWatch Events)* delivers a stream of real-time data from your applications, software as a service *(SaaS)* applications, and AWS services to targets such as AWS Lambda functions, HTTP invocation endpoints using API destinations, or event buses in other AWS accounts

#### Transfer Acceleration:
- Designed to optimize transfer speeds from across the world into S3 buckets
- Uses the globally distributed edge locations in Amazon CloudFront
- Use cases:
    - customers uploading to a centralized bucket from all over the world
    - transfering gigabytes to terabytes of data on a regular basis across continents

#### Requester Pays:
- The requester pays for requests and data transfer costs
- Anonymous access to this bucket is disabled

#### Static Website Hosting:
- Hosts a static website, where individual webpages include static content
- May also contain client-side script *(but not server-side scripts)*
- Website endpoints *(format varies per region)*
    - s3-website dash (-) Region ‐ `http://bucket-name.s3-website-Region.amazonaws.com`
    - s3-website dot (.) Region ‐ `http://bucket-name.s3-website.Region.amazonaws.com`
- Add a DNS CNAME to map a registered domain *(e.g. `http://www.example-bucket.com`)* to the bucket
- Create an index document to specify the home or default page of the website
    - `index.html`
- Create an error document to handle errors
    - `error.html`
