---
title : "Tạo role"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1.1 </b> "
---

1. Search từ khoá IAM trên thanh tìm kiếm dịch vụ của AWS, sau đó chọn dịch vụ IAM 
    ![CreateRole](/images/3/3.1.1.1.png)

2. Click chọn roles ở thanh menu bên trái, sau đó chọn create role
    ![CreateRole](/images/3/3.1.1.2.png)


3. Khởi tạo role với các thông số sau:
    - Trusted entity type: AWS service
    - Service or use case: System Manager
    - Choose a use case for the specified service: Use case Systems Manager
    - Sau đó click next
    ![CreateRole](/images/3/3.1.1.3.png)


    - Add permissions: tìm kiếm permission với từ khoá AmazonSSMAutomationRole, sau đó click vào ô checkbox rồi click next
    ![CreateRole](/images/3/3.1.1.4.png)

    - Role name: AssumeRole
    - Description: giữ mặc định
    ![CreateRole](/images/3/3.1.1.5.png)

    - Review lại và chọn create role
    ![CreateRole](/images/3/3.1.1.6.png)

  
  

4. Sau khi tạo role thành công, AWS sẽ chuyển trang web về trang Roles, sau đó chọn Role mới tạo ở trên, click vào tên role để vào trang xem chi tiết
    ![CreateRole](/images/3/3.1.1.7.png)


5. Ở trang chi tiết role, chọn tab Trust Relationship, chọn edit trust policy 
    ![CreateRole](/images/3/3.1.1.8.png)



6.  Copy đoạn code, chỉnh sửa lại nội dung cho phù hợp với account AWS sau đó paste vào phần text editor, rồi nhấn update policy

    ```json
    {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Sid": "",
                "Effect": "Allow",
                "Principal": {
                    "Service": [
                        "ssm.amazonaws.com"
                    ]
                },
                "Action": "sts:AssumeRole",
                "Condition": {
                    "StringEquals": {
                        "aws:SourceAccount": "<account id of aws>"
                    },
                    "ArnLike": {
                        "aws:SourceArn": "arn:aws:ssm:*:<account id of aws>:automation-execution/*"
                    }
                }
            }
        ]
    }
    ```
    ![CreateRole](/images/3/3.1.1.9.png)



7. Ở trang detail role, chọn tab Permissions, sau đó chọn add permission, chọn create inline policy 
    ![CreateRole](/images/3/3.1.1.10.png)


8. Khởi tạo với các thông số sau: 
    - Chọn JSON
    - copy đoạn code, sau đó paste vào ô textarea, sau đó chọn next
        ```json
        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": [
                        "s3:PutObject",
                        "s3:GetObject"
                    ],
                    "Resource": "arn:aws:s3:::<name of S3 bucket>/*"
                }
            ]
        }
        ```
        ![CreateRole](/images/3/3.1.1.11.png)


    - Nhập tên policy, review lại và chọn create policy
    ![CreateRole](/images/3/3.1.1.12.png)
  

9. Khởi tạo tiếp Inline policy với permission ec2:CreateSnapshot và ec2:DescribeSnapshots
    ```json
    {
        "Version":"2012-10-17",
        "Statement":[
            {
                "Effect":"Allow",
                "Action":"ec2:CreateSnapshot",
                "Resource":"*"
            },
            {
                "Effect":"Allow",
                "Action":"ec2:DescribeSnapshots",
                "Resource":"*"
            }
        ]
    }
    ```
    ![CreateRole](/images/3/3.1.1.13.png)
    ![CreateRole](/images/3/3.1.1.14.png)

















