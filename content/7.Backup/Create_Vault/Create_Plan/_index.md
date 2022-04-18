---
title: "Create Backup Plan"
chapter: false
weight: 20
pre:
---

## Creating a Backup Plan

`STEP 10:`  Navigate to the main AWS Backup service menu and select **Backup plans** from the left-hand menu.

`STEP 11:`  Select **Create Backup plan**.

`STEP 12:`  Select the **Build a new plan** radio button.

#### Plan Name:
- Define the name of the Backup Plan

`STEP 13:`  Enter "EBS-Daily-Plan."

#### Backup Rule Name:
- Rules to defining the schedule, window, and lifecycle

`STEP 14:`  Enter "EBS-Daily-Rule."

#### Backup Vault:
- Select the vault in which to store the backups

`STEP 15:`  Select the previously created "EBS-Vault" from the drop-down.

#### Backup frequency:
- How frequently to take and store snapshot backups
- For select data services, continuous backups for point-in-time recovery (PITR) is possible

`STEP 15:`  Select *Daily* from the drop-down.

#### Backup Window:
- Define the window for which the backups to initiate
    - **Start time**: set time for the window to begin
    - **Start within**: period in which the backup should start once the window begins (marked as *Expired* if they don't)
    - **Complete within**: period in which the backup should complete (marked as *Expired* if they don't)

`STEP 15:`  Select the *Customize backup window* radio button
- Enter a **Start time** of *01:30 AM UTC*.
- Select *2 hours* from the **Start within** drop-down.
- Select *3 days* from the **Complete within** drop-down.

#### Transition to Cold Storage:
- Move backups to cold storage
- Only currently available for certain data services

#### Retention Period:
- How long to keep the backups for automatically deleting them

`STEP 16:`  Select *Days* from the drop-down and enter a value of *3*.

#### Copy to Destination:
- Create cross-Region and cross-account copies of your recovery points

`STEP 17:`  Skip to the bottom of the page and select **Create plan**.
