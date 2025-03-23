---
title: "Storage Characteristics"
draft: false
weight: 40
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
    - Data durability can be reduced by factors such as hardware failures, natural disasters, human errors, cybersecurity threats, software glitches, and the lack of proper data governance and validation practices. 
- **Availability** is the percentage of time a network component or service is accessible to a user in a given period, usually defined as a year
    - Most AWS services offer between 3-5 9's of availability SLA (Route 53 is 100%)
    - Several factors can reduce data availability, including hardware failures, network issues, software problems, security breaches, and poor data management practices.

<img src='/images/avail-vs-dur.png' width='1000px'>

#### Durability Math Example for 99.999%
- 99.999% = 0.99999

- 1 - 0.99999 = 0.00001 *(representing object loss)*

- 0.00001 is one one-hundred thousandth, or 1 in 100,000

- 1 object loss in 100,000 years

#### Availability Math Example for 99.999%
- 99.999% = 0.99999

- 1 - 0.99999 = 0.00001 *(representing data non-availability)*

- 365 days x 24 hours x 60 minutes x 60 = 31,536,000 seconds *(number of seconds in one year)*

- 0.00001 x 31,536,000 seconds = 315.36 seconds

- 315.36 seconds / 60 = 5.256 minutes

- 0.256 x 60 ≈ 15 seconds

- 5 minutes and 15 seconds of non-availability in one year

{{% children showhidden="false" /%}}
