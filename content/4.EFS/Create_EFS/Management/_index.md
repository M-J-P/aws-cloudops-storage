---
title: "Management"
chapter: false
weight: 20
pre:
---

## Management of EFS

#### Lifecycle management:
1. Eliminates the risk of unbounded access charges while still providing low latencies
2. Autmoatic transistion to infrequently accessed storage, which is less expensive
    - Transition options include:
        - None
        - 7 days since last access
        - 14 days since last access
        - 30 days since last access
        - 60 days since last access
        - 90 days since last access
3. Automatic transition of files out of infrequently accessed storage
    - Transition options include:
        - None
        - On first access

<img src='/images/efs-transition.png' width='800px'>
