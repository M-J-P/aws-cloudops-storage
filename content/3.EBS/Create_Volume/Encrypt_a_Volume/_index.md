---
title: "Encrypt a Volume"
chapter: false
weight: 20
pre:
---

## A Bonus Exercise for Practice

#### Common AWS Architect Associate Exam Question:

- How do I encrypt my EBS volume's data if I didn't select an encrypted volume at the time of the EC2's creation?

##### STEPS:

1. Stop the EC2 instance.
2. Create an EBS snapshot of the volume to be encrypted.
3. Copy the EBS snapshot, encrypting the copy in the process using the desired key.
4. Using the new, encrpyted EBS snapsot, create a new EBS volume.  This volume will be encrypted.
5. Detach the original EBS volume and attach the new encrypted EBS volume, making sure to match the device name (e.g. /dev/xvda1, etc.)
6. Start the EC2 instance.
