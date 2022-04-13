---
title: "General Properties"
chapter: false
weight: 10
pre:
---

## General Properties of a Glacier Vault

#### Configuration:
- Names are unique per account
- Names between 1 and 255 characters long
- Allowed characters are a–z, A–Z, 0–9, '\_', '-', and '.'

`STEP 5:`  Notice how the region defaults to the overarching region in the AWS Console.

`STEP 6:`  Provide a *Vault Name*.

`STEP 7:`  Select **Next Step**.

#### Notifications:
- Messages sent when an S3 Glacier job completes
- Sent via the Amazon Simple Notification Service *(SNS)*
- Job completion triggers *(takes 3.5 to 4.5 hours)*:
    - archive retrieval
    - vault inventory retrieval

`STEP 8:`  Select the radio button for *Enable notifications and use an existing SNS topic*.

`STEP 9:`  Select **Next Step**.

`STEP 10:`  Under **Event Notifications Details** ...
- For **Amazon SNS Topic ARN** feel free to use the previously created SNS topic ARN or create a new one.
- Select the checkbox for **Archive Retrieval Job Complete**.
- Select the checkbox for **Vault Inventory Retrieval Job Complete**.

`STEP 11:`  Select **Next Step** and then **Submit**.

#### Tags:
- Define tags to categorize your bucket for discovery, analysis, and/or cost tracking
- Some labeling examples include:  by project, by owner, by application, by environment, by sensitivity
- Uses key-value pairs


#### Vault Lock:
- Add controls such as “write once read many” (WORM) in a vault lock policy
- Lock the policy from future edits
- Examples:
    - deny deletion permissions for archives less than 365 days old
    - deny deletion permissions based on a tag


`EXTRA EXERCISE:`  Update the S3 bucket lifecycle policy to transition to Glacier after 90 days.
