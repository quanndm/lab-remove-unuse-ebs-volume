---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Tổng quan

Trong bài lab này, bạn sẽ thực hành về xoá các <b>Amazon Elastic Block Store (Amazon EBS) volumes</b> không còn sử dụng nữa, bằng cách sử dụng <b>AWS Config</b> và <b>AWS Systems Manager</b>

Link AWS Prescriptive Guidance Patterns: [here](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/delete-unused-amazon-elastic-block-store-amazon-ebs-volumes-by-using-aws-config-and-aws-systems-manager.html)

Khi hoàn thành phần này, bạn sẽ triển khai kiến trúc hạ tầng như sau:
![structure](../../images/1/design.png)

- mô tả các bước:
    1. The AWS Config rule evaluates the EBS volumes.
    2. The rule returns a list of compliant and noncompliant resources. EBS volumes that are in the `available` state, which are unused volumes, are determined to be noncompliant.
    3. AWS Config automatically starts the Automation runbook.
    4. If configured, Systems Manager creates snapshots of the unused volumes before deleting them.
    5. Systems Manager deletes the unused EBS volumes.


##### AWS Config
- AWS Config là dịch vụ được quản lý hoàn toàn, cung cấp cho bạn thông tin kiểm kê tài nguyên AWS, lịch sử cấu hình và thông báo thay đổi cấu hình để đảm bảo bảo mật và khả năng kiểm soát. Config Rules cho phép bạn tạo các quy tắc tự động kiểm tra cấu hình của các tài nguyên AWS được ghi lại bởi AWS Config.
- Document: [here](https://aws.amazon.com/vi/config)

##### AWS Systems Manager
- AWS Systems Manager là dịch vụ quản lý giúp bạn tự động thu thập thông tin kiểm kê phần mềm, áp dụng các bản vá hệ điều hành, tạo hình ảnh hệ thống và định cấu hình hệ điều hành Windows và Linux. Những khả năng này giúp bạn xác định và theo dõi cấu hình hệ thống, ngăn ngừa sai lệch và duy trì sự tuân thủ của phần mềm cho các cấu hình EC2 và tại chỗ.
- Document: [here](https://aws.amazon.com/vi/systems-manager)

#### Nội dung

1. [Giới thiệu](1-introduce/)
2. [Các bước chuẩn bị](2-Preparation/)
3. [Cấu hình AWS Config](3-ConfigureAWSConfig/) 
4. [Cấu hình automatic remediation](4-ConfigureAutomationRemediation/)
5. [Dọn dẹp tài nguyên](5-CleanUp/)
