---
title : "Khởi chạy rule"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

1. Ở trang dashboard của AWS Config, chọn rules ở thanh menu, sau đó chọn add rule
   ![RunTheRule](/images/3/3.3.1.png)

2. Thêm rule mới với các tham số sau
   - Select rule type: Add AWS managed rule
   - AWS Managed Rules: tìm kiếm với từ khoá ec2-volume, sau đó chọn ec2-volume-inuse-check
   - click next 
   ![RunTheRule](/images/3/3.3.2.png)


   - Evaluation mode:
     - Scope of changes: All changes
   - Parameters: click remove
   - giữ mặc định các tham số còn lại, chọn next
   ![RunTheRule](/images/3/3.3.3.png)


   - Review lại và click save
   ![RunTheRule](/images/3/3.3.4.png)


3. Trở về trang Rules, click chọn name của rule mới tạo để xem chi tiết
   ![RunTheRule](/images/3/3.3.5.png)


4. Kiểm tra volume trong phần Resources in scope
   ![RunTheRule](/images/3/3.3.6.png)



5.  So sánh với volume trong EC2
   ![RunTheRule](/images/3/3.3.7.png)
  

{{% notice  note %}}
Như vậy ta đã tạo được AWS config với rule là ec2 volume đang sử dụng, volume nào không được sử dụng/attach vào ec2 thì sẽ được show ở list Resources in scope là Noncompliant
{{% /notice %}}






