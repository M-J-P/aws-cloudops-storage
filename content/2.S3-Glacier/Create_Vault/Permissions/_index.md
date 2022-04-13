---
title: "Permissions"
chapter: false
weight: 30
pre:
---

## S3 Glacier Permissions

#### Vault Access Policy:
- Include any additional access policies beyond IAM policies
- An example to provide MFA before deletion:

```
{
    "Version": "2012-10-17",
    "Statement": [
       {
          "Sid": "add-mfa-delete-requirement",
          "Principal": {
             "AWS": [
                "arn:aws:iam::123456789012:root"
             ]
          },
          "Effect": "Allow",
          "Action": [
             "glacier:Delete*"
          ],
          "Resource": [
             "arn:aws:glacier:us-west-2:999999999999:vaults/examplevault"
          ],
          "Condition": {
             "Bool": {
                "aws:MultiFactorAuthPresent": true
             }
          }
       }
    ]
}
```
