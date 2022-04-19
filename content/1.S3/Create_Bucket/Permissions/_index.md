---
title: "Permissions"
chapter: false
weight: 30
pre:
---

## S3 Bucket Permissions

#### IAM policy:
1. Applies to users, groups, and roles (i.e. principals)
2. Specify what **actions** are allowed or denied on what AWS resources for a **principal**
3. Best used when ansering the question:  *"What can this user do in AWS?"*
4. Written in JSON
5. Example:

```
{
  "Version": "2012-10-17",
  "Statement":[{
    "Effect": "Allow",
    "Action": "s3:*",
    "Resource": ["arn:aws:s3:::my_bucket",
                 "arn:aws:s3:::my_bucket/*"]
    }
  ]
}
```

#### Bucket policy:
1. Applies ONLY to bucket to which it's attached
2. Provides access to the objects stored in the bucket
3. Don't apply to objects owned by other accounts
4. Elements:
    - Principal – The account or user who is allowed access to the **actions** and **resources** in the statement
    - Effect – What the effect will be:  **allow** or **deny**
        - default is to **deny**
        - **allow** must be explicitly granted 
        - is possible to explicitly **deny** access to a resource
        - use case:  to make sure that a user can't access the resource, even if a different policy grants access
    - Actions – a set of operations *(APIs)* can be allowed (or denied)
    - Resources – uses the Amazon Resource Name *(ARN)* to identify the resource for which one can allow or deny permissions
5. Best used when ansering the question:  *"Who can access this S3 bucket?"*
6. Written in JSON
7. Example:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": ["arn:aws:iam::111122223333:user/Alice",
                "arn:aws:iam::111122223333:root"]
      },
      "Action": "s3:*",
      "Resource": ["arn:aws:s3:::my_bucket",
                   "arn:aws:s3:::my_bucket/*"]
    }
  ]
}
```
- See other S3 bucket policies examples here:  https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html

#### Access Control List (ACL)
1. Apply to BOTH buckets AND objects
2. Defines which AWS accounts or groups are granted access and the type of access
3. S3 ACLs is a legacy access control mechanism that predates IAM; IAM and Bucket policies are recommended instead

#### Cross-origin resource sharing (CORS):

<img src='/images/cors.png' width='800px'>

1. Defines a way for client web applications that are loaded in one domain to interact with resources in a different domain 
2. Enables rich, client-side web applications
3. Written in JSON or XML
4. Example:

```
[
    {
        "AllowedHeaders": [
            "*"
        ],
        "AllowedMethods": [
            "PUT",
            "POST",
            "DELETE"
        ],
        "AllowedOrigins": [
            "http://www.example.com"
        ],
        "ExposeHeaders": [
            "x-amz-server-side-encryption",
            "x-amz-request-id",
            "x-amz-id-2"
        ],
        "MaxAgeSeconds": 3000
    }
]
```
