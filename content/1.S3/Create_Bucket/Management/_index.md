---
title: "Management"
chapter: false
weight: 40
pre:
---

## Management of an S3 Bucket

#### Lifecycle Rules:
1. Manage objects throughout their lifecycle so that they are stored cost effectively.
2. A set of rules that define actions:
    - transition actions:  move objects to a less expensive storage class after a certain period of time
    - expiration actions:  delete objects after a certain period of time
3. Filter objects to be transitioned by:
    - prefix
    - tags
    - size

`STEP 28:`  Navigate to the **Management** tab and select **Create lifecycle rule**.

`STEP 29:`  Under **Lifecycle rule configuration** ...
- Provide a rule name (e.g. transition-to-IA)
- Select the *Apply to all objects in the bucket* radio button and acknowledge it.

`STEP 30:`  Under **Lifecycle rule actions**, select these checkboxes ...
- *Move current versions of objects between storage classes*
- *Move noncurrent versions of objects between storage classes*
- *Delete expired object delete markers or incomplete multipart uploads*

`STEP 31:`  Under **Transition current versions of objects between storage classes** ...
- Choose a *Standard-IA* transition from the drop-down.
- Enter "1" for the number of days.  What message is shown?  Correct and enter "30" for the number of days.

`STEP 32:`  Repeat for **Transition non-current versions of objects between storage classes** ...

`STEP 33:`  Select both checkboxes under **Delete expired object delete markers or incomplete multipart uploads**.
- Enter "1" for the number of days.

`STEP 34:`  Select **Create rule** at the bottom of the page.


#### Replication Rules:
1. Enables automatic, asynchronous copying of objects across Amazon S3 buckets
    - Same-Region Replication (SRR)
    - Cross-Region Replication (CRR)
2. To a single destination bucket or to multiple destination buckets
3. Replicate all objects or designate a filter
    - filter by prefix
    - filter by tag
4. Preserve encryption if desired
5. Uses cases:
    - Replicate objects while retaining metadata
    - Replicate objects into different storage classes
    - Maintain object copies under different ownership
    - Keep objects stored over multiple AWS Regions

`STEP 35:`  Navigate back to the Buckets Dashboard and create a new bucket in a different region than the existing one.
- When creating the new bucket, copy the settings from the first bucket.

`STEP 36:`  After creating the new bucket, select the original bucket, and navigate to the **Management** tab and select **Create replication rule**.

`STEP 37:`  Under **Replication rule configuration** ...
- Provide a rule name (e.g. replication-rule).
- Leave the **Status** radio button as *Enabled*.
- Under **Source Bucket** select the *Apply to all objects in the bucket* radio button

`STEP 38`  Under **Destination** choose the newly created bucket as the destination.

`STEP 39`  Under **IAM role** select *Create new role* from the drop-down.

`STEP 40`  Under **Storage class** change the storage class to *One Zone-IA*.

`STEP 41`  At the bottom of the page, select **Create replication**.
- Choose "No" when prompted for a one-time batch operation and select **Submit**.
- Notice the auto-created IAM role.

`STEP 42:`  Return to the **Management** tab for this bucket and notice the existing rules.
