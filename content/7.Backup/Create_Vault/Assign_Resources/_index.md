---
title: "Assign Resources"
chapter: false
weight: 30
pre:
---

## Assigning Resources to a Plan

`STEP 18:`  Select **Assign resources**.

#### General:

`STEP 19:`  Enter *EBS* as the **Resource assignment name**.

`STEP 20:`  For **IAM role**, leave the radio button as-is.

#### Define Resource Selection:
- Select which resource types are to be included in this plan

`STEP 21:`  Select the **Include specific resource types** radio button.

`STEP 22:`  From the **Select specific resource types** drop-down, choose the *EBS* checkbox.
- *(this defaults to **All volumes**, but you could also just select the previously created EBS volume.)*

#### Refine Selection with Tags:
- Use tags to drive backups

`STEP 23:`  Enter these values:
- **Key** ==> *EBS-Backup-Daily*
- **Condition for value** ==> *Equals*
- **Value** ==> *TRUE*

`STEP 24:`  Skip to the bottom of the page and select **Assign resources**.

`STEP 25:`  Wait until tomorrow and return to the AWS Backup service.  Look under the **Dashboad** to see if your EBS volume has been backed up.
