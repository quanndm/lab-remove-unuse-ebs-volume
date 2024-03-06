---
title : "Create EC2"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
#### Tạo EC2

Purpose: When initializing EC2, by default the EBS volume will be initialized and attached to EC2

1. Search EC2 on Amazon's service search bar, then select EC2 service to go to the dashboard page
![CreateEC2](../../images/2/2.1.1.png)

2. On the EC2 service dashboard page, select launch instance
![CreateEC2](../../images/2/2.1.2.png)

3. On the EC2 service dashboard page, select launch instance
    - Name: Type name of EC2 instance
    ![CreateEC2](../../images/2/2.1.3.png)

    - Application and OS Images (Amazon Machine Image): Amazon Linux 2023
    ![CreateEC2](../../images/2/2.1.4.png)

    - Instance type: t2.micro
    - Key pair (login): proceed without a key pair
    ![CreateEC2](../../images/2/2.1.5.png)

    - Network settings:
        - Click edit
        - Firewall: Select existing security group
        - choose default VPC
        - The remaining options keep default
        - click launch instance
        ![CreateEC2](../../images/2/2.1.6.png)       

4. After launching the instance successfully, click view all resources at the bottom of the page
    ![CreateEC2](../../images/2/2.1.7.png)       

5. On the instances page, click on the newly created EC2 instance, select the storage tab and click on the volume ID
    ![CreateEC2](../../images/2/2.1.8.png)

6. Click to select the volume, and check the operating status of the volume, the correct status of the volume when it is attached to EC2 is in-use
    ![CreateEC2](../../images/2/2.1.9.png)