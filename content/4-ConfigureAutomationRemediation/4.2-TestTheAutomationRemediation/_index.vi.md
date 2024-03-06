---
title : "Kiểm tra automation remediation action"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---
1. Vào trang AWS Config dashboard, chọn Rules, chọn ec2-volume-inuse-check, nhấn chọn actions, chọn re-evaluate
   ![TestAction](/images/4/4.2.1.png)
 

   ![TestAction](/images/4/4.2.2.png)


   ![TestAction](/images/4/4.2.3.png)

 

2. Kiểm tra lại volume
   - Vào EC2 dashboard, click chọn volumes ở thanh menu, review list volume hiện có
   ![TestAction](/images/4/4.2.4.png)

   - Kiểm tra snapshot, click chọn snapshot ở thanh menu, có 1 snapshot được tạo ra từ việc copy 1 volume
   ![TestAction](/images/4/4.2.5.png)

  
{{% notice note %}}
trường hợp không thể xoá volume có thể attach thêm EC2 full access policy vào AssumeRole
{{% /notice %}}

