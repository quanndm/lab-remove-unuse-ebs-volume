---
title : "Attach policy"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.1.2 </b> "
---


1. From the IAM dashboard page, click on roles in the menu bar, click on the name of the previously created role to go to the role details page.
    ![AttachPolicy](../../../image/3/3.1.2.1.png)

2. In the summary section, click copy ARN
    ![AttachPolicy](../../../image/3/3.1.2.2.png)


3. Select the Permission tab, select Add permissions, then select Create inline policy
    ![AttachPolicy](../../../image/3/3.1.2.3.png)


4. Initialize policy with the following parameters:
    - Choose Visual
    - Service: IAM
    - filter actions: Search with keyword PassRole, then click PassRole
    - Resource: Specific
    - click  Add ARN
    ![AttachPolicy](../../../image/3/3.1.2.4.png)


    - Paste the RNA copied above into the RNA resource box, then click add ARNs
    ![AttachPolicy](../../../image/3/3.1.2.5.png)


    - Click next 
    ![AttachPolicy](../../../image/3/3.1.2.6.png)


    - Enter the policy name, and click create policy
    ![AttachPolicy](../../../image/3/3.1.2.7.png)













