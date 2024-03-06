---
title : "Tạo EC2"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
#### Tạo EC2

Mục đích: Khi khởi tạo EC2, mặc định EBS volume sẽ được khởi tạo và attach vào chung với EC2

1. Search EC2 trên thanh tìm kiếm service của Amazon, sau đó chọn EC2 service để vào trang dashboard
![CreateEC2](/images/2/2.1.1.png)

2. Ở trang dashboard của EC2 service, chọn launch instance
![CreateEC2](/images/2/2.1.2.png)

3. Ở trang Launch an instance, 
    - Name: nhập name của EC2 instance
    ![CreateEC2](/images/2/2.1.3.png)

    - Application and OS Images (Amazon Machine Image): Amazon Linux 2023
    ![CreateEC2](/images/2/2.1.4.png)

    - Instance type: t2.micro
    - Key pair (login): proceed without a key pair
    ![CreateEC2](/images/2/2.1.5.png)

    - Network settings:
        - Click edit
        - Firewall: Select existing security group
        - chọn default VPC
        - các tuỳ chọn còn lại giữ mặc định
        - nhấn chọn launch instance
        ![CreateEC2](/images/2/2.1.6.png)       

4. Sau khi launch instance thành công, click chọn view all resources ở cuối trang
    ![CreateEC2](/images/2/2.1.7.png)       

5. Ở trang instances, click chọn EC2 instance mới tạo, chọn tab storage và click vào ID của volume
    ![CreateEC2](/images/2/2.1.8.png)

6. Click chọn volume, và kiểm tra trạng thái hoạt động của volume, trạng thái đúng của volume khi attch vào EC2 là in-use
    ![CreateEC2](/images/2/2.1.9.png)