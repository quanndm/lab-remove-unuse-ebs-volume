---
title : "Clean up resource"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---


1.  Delete Remediation action
    - Go to the AWS Config role details page, in the Remediation action section, click delete
    ![cleanup](../image/5/5.1.png)
    - type confirm, then click delete
    ![cleanup](../image/5/5.2.png)

2. Delete rule
    - Select the rule to delete in the lab
    - click actions
    - click delete rule
    ![cleanup](../image/5/5.3.png)

    - type confirm, click delete
    ![cleanup](../image/5/5.4.png)

3. Delete AWS config
    - command delete aws config, change region to match the account
        ```
        aws configservice delete-configuration-recorder --configuration-recorder-name default --region <region-name>
        ```
    - On Dashboard of AWS page, click cloudshell at bottom of the left corner
    ![cleanup](../image/5/5.5.png)
    - Paste command copy above then press enter    
    ![cleanup](../image/5/5.6.png)
    - Check AWS Config Layout 
    ![cleanup](../image/5/5.7.png)

4. Delete EC2
    - In the EC2 dashboard, click on the instance in the menu, click on the instance to delete, select instance state, select terminate instance
    ![cleanup](../image/5/5.8.png)
    - Choose terminate
    ![cleanup](../image/5/5.9.png)

5. Delete Snapshot
    - On the EC2 dashboard page, select snapshots in the menu bar, select the snapshot to delete, click actions, select delete snapshot
    ![cleanup](../image/5/5.10.png)
    - Click delete
    ![cleanup](../image/5/5.11.png)

6. Delete S3 bucket
    - Ở trang S3 dashboard, chọn buckets ở thanh menu, chọn bucket cần xoá, nhấn chọn empty
    ![cleanup](../image/5/5.12.png)
    - On the S3 dashboard page, select buckets in the menu bar, select the bucket to delete, click empty
    ![cleanup](../image/5/5.13.png)
    - After successfully emptying the bucket, select the bucket you want to delete and click delete
    ![cleanup](../image/5/5.14.png)
    - Enter the S3 bucket name, then click delete bucket
    ![cleanup](../image/5/5.15.png)
