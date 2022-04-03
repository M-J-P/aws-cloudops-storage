---
title: "General Properties"
chapter: false
weight: 10
pre:
---

## General Properties of a Glacier Vault

#### Configuration:
1. Names are unique per account
2. Names between 1 and 255 characters long
3. Allowed characters are a–z, A–Z, 0–9, '\_', '-', and '.'

#### Notifications:
1. Messages sent when an S3 Glacier job completes
2. Sent via the Amazon Simple Notification Service *(SNS)*
3. Job completion triggers *(takes 3.5 to 4.5 hours)*:
    - Archive retrieval
    - Vault inventory retrieval

#### Tags:
1. Define tags to categorize your bucket for discovery, analysis, and/or cost tracking
2. Some labeling examples include:  by project, by owner, by application, by environment, by sensitivity
3. Uses key-value pairs


#### Vault Lock:
1. Add controls such as “write once read many” (WORM) in a vault lock policy
2. Lock the policy from future edits
3. Examples:
    - Deny deletion permissions for archives less than 365 days old
    - Deny deletion permissions based on a tag
