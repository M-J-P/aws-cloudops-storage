---
title: "General Properties"
chapter: false
weight: 10
pre:
---

## General Properties of an S3 Bucket

#### Configuration:
- A unique name to describe the bucket
- A region in which the bucket is to be created

`STEP 6:`  Choose a unique name for your bucket

`STEP 7:`  Select the **us-east-1** region for your bucket

#### Object Ownership:
- ACL Disabled *(recommended)*:  ensures that every object in the bucket is owned by the account owner
- ACL Enabled:  allows for other accounts to own an object that they write to this bucket

`STEP 8:`  Toggle the radio button under **Object Ownership**.
    - Notice the difference

`STEP 9:`  Toggle the radio button back to *ACL disabled*.

#### Public Access:
- Buckets are private by default, where objects can only be accessed within the account
- To make objects public, disable the default and select any additional protections
- Specifically acknowledge if a bucket is to have a public configuration

`STEP 10:`  Uncheck the checkbox under **Block Public Access settings for this bucket**.
    - Notice the difference

`STEP 11:`  Re-check the checkbox.

#### Versioning:
- Allows for keeping multiple variants of an object in the same bucket
- Used to preserve, retrieve, and restore every version of every object stored in your Amazon S3 bucket
- Versioning is often required for additional bucket capabilities *(e.g. Life Cycle Policies, Backups)*

`STEP 12:`  Toggle this radio button under **Bucket Versioning**.
- Leave it on *enabled*.

#### Tags:
- Define tags to categorize your bucket for discovery, analysis, and/or cost tracking
- Some labeling examples include:  by project, by owner, by application, by environment, by sensitivity
- Uses key-value pairs

`STEP 13:`  Select Add Tag under **Tags**.
- Define the Key as "Environment"
- Define the Value as "PROD

#### Encryption:
- Protect your objects by encrypting them via:
    - Amazon S3-managed keys *(SSE-S3)*
    - keys stored in AWS Key Management Service *(SSE-KMS)*

`STEP 14:`  Toggle the radio buttons under **Default encryption**.
- Leave the encryption type as *Amazon S3-managed keys (SSE-S3)*
    - *(but feel free to play around)*
- Leave it on *Enable*.

#### Object Lock:
- Store objects using a write-once-read-many *(WORM)* model
- Pevent objects from being deleted or overwritten for a fixed amount of time or indefinitely
- Define retention periods through a bucket policy

`STEP 15:`  Select **Create Bucket** at the bottom of the page.
