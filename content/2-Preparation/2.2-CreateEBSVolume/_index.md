---
title : "Create EBS Volume"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---
#### Create  EBS volume

Purpose: Create an empty volume, convenient for aws config and aws management system to check usage status

1. Search EC2 on Amazon's service search bar, then select EC2 service to go to the dashboard page
    ![CreateEBSVolume](/images/2/2.2.1.png)

2. Select volumes in the left sidebar, then select create volume
    ![CreateEBSVolume](/images/2/2.2.2.png)

3. On Create volume page,
    - Volume type: gp2
    - size: 8gb
    ![CreateEBSVolume](/images/2/2.2.3.png)

    - Keep the remaining options as default, then click create volume
    ![CreateEBSVolume](/images/2/2.2.4.png)

4. On the Volumes page, select the newly created volume and check the volume's status. By default, after the volume is successfully created and not in use, the volume's status will be Available.
    ![CreateEBSVolume](/images/2/2.2.5.png)




