---
title : "Cấu hình AWS Config"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---

#### Cấu hình AWS Config

Trong phần này, chúng ta sẽ bắt đầu cấu hình AWS Config, bao gồm việc tạo role cho automation runbook, khởi động AWS Config recorder, tạo và khởi chạy rule đã thiết lập trong AWS Config 

AWS Config recorder được sử dụng để lưu trữ lịch sử các sự thay đổi cấu hình của 1 hay nhiều tài nguyên AWS. Tiện lợi cho việc audit các vấn đề liên quan đến tài nguyên, kết hợp dịch vụ AWS Cloudtrail

AWS Config Rule cho phép bạn set các rule dựa trên AWS common hoặc custom rule do bạn define. Ví dụ, bạn có thể đảm bảo AWS EBS được encrypted, EC2 Instance được gán tag, EIP được attach đến EC2, kiểm tra EBS volume có được sử dụng hay không,... Ngoài ra, cho phép monitor sự thay đổi của AWS resource và cung cấp 1 new dashboard để track.


#### Nội dung

1. [Tạo role cho Automation runbook](3.1-CreateRole/)
2. [Khởi động AWS Config Recorder ](3.2-TurnOnAWSConfigRecorder/)
3. [Run the rule](3.3-RunTheRule/)
