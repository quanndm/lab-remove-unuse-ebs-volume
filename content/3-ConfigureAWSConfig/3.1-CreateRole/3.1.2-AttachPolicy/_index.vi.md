---
title : "Attach Policy"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 3.1.2 </b> "
---

1. Từ trang dashboard của IAM, click chọn roles bên thanh menu, click vào tên của role đã tạo trước đó để vào trang chi tiết role
    ![AttachPolicy](../../../image/3/3.1.2.1.png)

2. Ở mục summary, click copy ARN
    ![AttachPolicy](../../../image/3/3.1.2.2.png)


3. Chọn Permission tab, chọn Add permissions, sau đó chọn Create inline policy
    ![AttachPolicy](../../../image/3/3.1.2.3.png)


4. Khởi tạo policy với các tham số sau:
    - Chọn Visual
    - Service: IAM
    - filter actions: tìm với từ khoá PassRole, sau đó click chọn PassRole
    - Resource: Specific
    - click chọn Add ARN
    ![AttachPolicy](../../../image/3/3.1.2.4.png)


    - Paste ARN đã copy ở trên vào ô resource ARN, sau đó click add ARNs
    ![AttachPolicy](../../../image/3/3.1.2.5.png)


    - Click next 
    ![AttachPolicy](../../../image/3/3.1.2.6.png)


    - Nhập policy name, và nhấn create policy
    ![AttachPolicy](../../../image/3/3.1.2.7.png)













