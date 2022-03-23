---
title: "Advanced Properties"
chapter: false
weight: 20
pre:
---

## Advanced Properties of an S3 Bucket

#### Intelligent-Tiering Configuration:
1. Set optimization for objects that will be rarely accessed for long periods of time

#### Server Access Logging:
1. Provides detailed records for the requests that are made to a bucket
2. Access log information can be useful in security and access audit
3. Learn about your customer base and understand your Amazon S3 bill

#### AWS CloudTrail data events:
1. Provides a record of actions *(events)* taken by a user, role, or an AWS service in Amazon S3
2. Can enable continuous delivery of CloudTrail events to an Amazon S3 bucket

#### Event Notifications:
1. Send a notification message to a destination whenever those events occur:
    - Amazon SNS
    - Amazon SQS
    - Lambda
2. General configuration:
    - Define an event name
    - Use prefix *(e.g. logical folders)*
    - Use suffix *(e.g. file extensions)*
3. Event types:
    - Object created
    - Object removed
    - Object restored
    - Lifecycle
    - Others
4. Amazon EventBridge *(f.k.a. Amazon CloudWatch Events)* delivers a stream of real-time data from your applications, software as a service *(SaaS)* applications, and AWS services to targets such as AWS Lambda functions, HTTP invocation endpoints using API destinations, or event buses in other AWS accounts

#### Transfer Acceleration:
1. Designed to optimize transfer speeds from across the world into S3 buckets
2. Uses the globally distributed edge locations in Amazon CloudFront
3. Use cases:
    - customers uploading to a centralized bucket from all over the world
    - transfering gigabytes to terabytes of data on a regular basis across continents

#### Requester Pays:
1. The requester pays for requests and data transfer costs
2. Anonymous access to this bucket is disabled

#### Static Website Hosting:
1. Hosts a static website, where individual webpages include static content
2. May also contain client-side script *(but not server-side scripts)*
3. Website endpoints *(format varies per region)*
    - s3-website dash (-) Region ‐ `http://bucket-name.s3-website-Region.amazonaws.com`
    - s3-website dot (.) Region ‐ `http://bucket-name.s3-website.Region.amazonaws.com`
4. Add a DNS CNAME to map a registered domain *(e.g. `http://www.example-bucket.com`)* to the bucket
5. Create an index document to specify the home or default page of the website
    - `index.html`
5. Create an error document to handle errors
    - `error.html`
