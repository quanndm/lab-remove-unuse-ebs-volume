---
title : "Create a Role for Automation runbook"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1.1 </b> "
---

1. Search for the keyword IAM on the AWS services search bar, then select the IAM service
    ![CreateRole](/images/3/3.1.1.1.png)

2. Click roles in the left menu bar, then select create role
    ![CreateRole](/images/3/3.1.1.2.png)


3. Initialize the role with the following parameters:
    - Trusted entity type: AWS service
    - Service or use case: System Manager
    - Choose a use case for the specified service: Use case Systems Manager
    - Then click next
    ![CreateRole](/images/3/3.1.1.3.png)


    - Add permissions: search for permissions with the keyword AmazonSSMAutomationRole, then click on the checkbox and click next
    ![CreateRole](/images/3/3.1.1.4.png)

    - Role name: AssumeRole
    - Description: keep default
    ![CreateRole](/images/3/3.1.1.5.png)

    - Review and select create role
    ![CreateRole](/images/3/3.1.1.6.png)

  
  

4. After successfully creating the role, AWS will move the website to the Roles page, then select the newly created Role above, click on the role name to go to the details page.
    ![CreateRole](/images/3/3.1.1.7.png)


5. On the role details page, select the Trust Relationship tab, select edit trust policy
    ![CreateRole](/images/3/3.1.1.8.png)



6.  Copy the code, edit the content to suit your AWS account, then paste it into the text editor, then click update policy

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



7. On the role detail page, select the Permissions tab, then select add permission, select create inline policy
    ![CreateRole](/images/3/3.1.1.10.png)


8. Initialize with the following parameters:
    - Choose JSON
    - Copy the code, then paste it into the textarea box, then select next
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


    - Enter the policy name, review it and select create policy
    ![CreateRole](/images/3/3.1.1.12.png)
  

9. Create Inline policy with permission ec2:CreateSnapshot and ec2:DescribeSnapshots
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
