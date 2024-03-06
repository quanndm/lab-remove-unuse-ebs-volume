---
title : "Tạo EBS volume"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo EBS volume

Mục đích: Khởi tạo 1 volume trống, thuận tiện cho việc aws config và aws management system check trạng thái sử dụng

1. Search EC2 trên thanh tìm kiếm service của Amazon, sau đó chọn EC2 service để vào trang dashboard
    ![CreateEBSVolume](/images/2/2.2.1.png)

2. Chọn tiếp volumes ở sidebar bên trái, sau đó chọn create volume
    ![CreateEBSVolume](/images/2/2.2.2.png)

3. Ở trang Create volume,
    - Volume type: chọn gp2
    - size: 8gb
    ![CreateEBSVolume](/images/2/2.2.3.png)

    - Giữ mặc định các tuỳ chọn còn lại, sau đó nhấn chọn create volume
    ![CreateEBSVolume](/images/2/2.2.4.png)

4. Ở trang Volumes, chọn volume mới tạo và kiểm tra trạng thái của volume, mặc định sau khi tạo volume thành công và không được sử dụng thì trạng thái của volume sẽ là Available 
    ![CreateEBSVolume](/images/2/2.2.5.png)




