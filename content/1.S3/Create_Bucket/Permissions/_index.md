---
title: "Permissions"
chapter: false
weight: 30
pre:
---

## S3 Bucket Permissions

#### Bucket policy:
1. Applies ONLY to buckets
2. Provides access to the objects stored in the bucket
3. Don't apply to objects owned by other accounts
4. Elements:
    - Principal – The account or user who is allowed access to the **actions** and **resources** in the statement
    - Effect – What the effect will be:  **allow** or **deny**
        - default is to **deny**
	- **allow** must be explicitly granted 
	- is possible to explicitly **deny** access to a resource
	    - use case:  to make sure that a user can't access the resource, even if a different policy grants access
    - Actions – a set of operations *(APIs)* can be allowed (or denied)
    - Resources – uses the Amazon Resource Name *(ARN)* to identify the resource for which one can allow or deny permissions
5. Written in JSON
6. Example:
    - **TO DO:  ADD IMAGE HERE**

#### Access Control List (ACL)
1. Apply to BOTH buckets AND objects
2. Defines which AWS accounts or groups are granted access and the type of access

#### Cross-origin resource sharing (CORS):
1. Defines a way for client web applications that are loaded in one domain to interact with resources in a different domain 
2. Enables rich, client-side web applications
3. Written in JSON
4. Example:
    - **TO DO:  ADD IMAGE HERE**
