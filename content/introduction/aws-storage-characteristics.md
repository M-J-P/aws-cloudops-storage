---
title: "Storage Characteristics"
draft: false
weight: 3
---

<img src='/images/storage-characteristics.png' width='1000px'>

#### Understanding Durability
- 11 9’s of durability is greater than most organizations would be able to accomplish on their own
- 11 9’s of durability corresponds to a loss of an object every 10,000 years out of 10M objects stored

<img src='/images/durability.png' width='1000px'>

#### Durability versus Availability
- **Durability** is a level that corresponds to an average annual expected loss of an object
    - AWS storage services focus more around durability for customers’ critical data
    - Example:  if 10,000 objects are stored with Amazon S3 (11 9's), one can on average expect to incur a loss of a single object once every 10,000,000 years
- **Availability** is the percentage of time a network component or service is accessible to a user in a given period, usually defined as a year
    - Most AWS services offer between 3-5 9's of availability SLA (Route 53 is 100%)

<img src='/images/avail-vs-dur.png' width='1000px'>


{{% children showhidden="false" %}}
