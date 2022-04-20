---
title: "Create an SNS Topic"
chapter: false
weight: 10
pre:
---

## Create an SNS Topic 

`STEP 1:`  Open another AWS Console tab through a preferred method (e.g. duplicate the tab).

`STEP 2:`  Search for and navigate to the **Simple Notification Service** (SNS).

`STEP 3:`  Open the left-hand menu (if not already open) and select **Topics**.

`STEP 4:`  Select **Create topic**.

`STEP 5:`  Under **Details** ...
- Select the *Standard* radio button.
- Provide a topic name (e.g. s3-bucket-notification).

`STEP 6:`  Skip to the bottom of the page and select **Create topic**.

`STEP 7:`  Copy the ARN for this topic (example:  *arn:aws:sns:us-east-1:111122223333:myTopic*) and save it to a temporary location.

`STEP 8:`  Select **Edit**.

`STEP 9:`  Expand the **Access policy** section and replace the existing policy with the below
- where the three tagged <> sections should use your values; the "<" and ">" are to be removed.

```
{
  "Version": "2012-10-17",
  "Id": "example-ID",
  "Statement": [
    {
      "Sid": "Example SNS topic policy",
      "Effect": "Allow",
      "Principal": {
        "Service": "s3.amazonaws.com"
      },
      "Action": "SNS:Publish",
      "Resource": "<YOUR SNS TOPIC ARN>",
      "Condition": {
        "StringEquals": {
          "aws:SourceAccount": "<YOUR ACCOUNT ID>"
        },
        "ArnLike": {
          "aws:SourceArn": "arn:aws:s3:*:*:<YOUR S3 BUCKET>"
        }
      }
    }
  ]
}
```

## Create an SNS Subscription

`STEP 10:`  Select **Create subscription**.

`STEP 11:`  Under **Details** ...
- Select *Email* from the **Protocol** drop-down.
- Provide an email address to which you have access during this class.


`STEP 12:`  Skip to the bottom of the page and select **Create subscription**.

## Confirm your subscription

`STEP 13:`  Open the received email and select **Confirm subscription**.

`STEP 14:`  Navigate back to the S3 service.
