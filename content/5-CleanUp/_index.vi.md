---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

1.  Xoá Remediation action
    - Vào trang chi tiết role của AWS Config, ở mục Remediation action, nhấn delete
    ![cleanup](/images/5/5.1.png)
    - nhập confirm, và nhấn delete
    ![cleanup](/images/5/5.2.png)

2. Xoá rule
    - Chọn rule cần xoá trong bài lab
    - click actions
    - click delete rule
    ![cleanup](/images/5/5.3.png)

    - nhập confirm, nhấn delete
    ![cleanup](/images/5/5.4.png)

3. Xoá AWS config
    - command xoá aws config, thay region phù hợp với account
        ```
        aws configservice delete-configuration-recorder --configuration-recorder-name default --region <region-name>
        ```
    - ở trang dashboard của AWS, chọn cloudshell ở cuối trang góc trái
    ![cleanup](/images/5/5.5.png)
    - nhập command copy trên và nhấn enter    
    ![cleanup](/images/5/5.6.png)
    - Kiểm tra lại AWS Config Layout đã trở về ban đầu
    ![cleanup](/images/5/5.7.png)

4. Xoá EC2
    - Ở EC2 dashboard, click chọn instance ở menu, nhấn chọn instance cần xoá, chọn instance state, chọn terminate instance
    ![cleanup](/images/5/5.8.png)
    - Click chọn terminate
    ![cleanup](/images/5/5.9.png)

5. Xoá Snapshot
    - Ở trang EC2 dashboard, chọn snapshots ở thanh menu, chọn snapshot cần xoá, click actions, chọn delete snapshot
    ![cleanup](/images/5/5.10.png)
    - Click delete
    ![cleanup](/images/5/5.11.png)

6. Xoá S3 bucket
    - Ở trang S3 dashboard, chọn buckets ở thanh menu, chọn bucket cần xoá, nhấn chọn empty
    ![cleanup](/images/5/5.12.png)
    - Nhập permanently delete, sau đó nhấn empty
    ![cleanup](/images/5/5.13.png)
    - Sau khi empty bucket thành công, chọn lại bucket cần xoá, click delete
    ![cleanup](/images/5/5.14.png)
    - Nhập tên S3 bucket, sau đó nhấn delete bucket
    ![cleanup](/images/5/5.15.png)
