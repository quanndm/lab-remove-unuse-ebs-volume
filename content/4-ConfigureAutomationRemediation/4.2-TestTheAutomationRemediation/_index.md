---
title : "Test the automation remediation action"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

1. Go to the AWS Config dashboard, select Rules, select ec2-volume-inuse-check, click actions, select re-evaluate
   ![TestAction](/images/4/4.2.1.png)
 

   ![TestAction](/images/4/4.2.2.png)


   ![TestAction](/images/4/4.2.3.png)

 

2. Check the volume again
   - Go to EC2 dashboard, click on volumes in the menu bar, review the list of available volumes
   ![TestAction](/images/4/4.2.4.png)

   - Check the snapshot, click on snapshot in the menu bar, there is a snapshot created from copying a volume
   ![TestAction](/images/4/4.2.5.png)

  
{{% notice note %}}
In case you cannot delete the volume, you can attach an EC2 full access policy to AssumeRole
{{% /notice %}}

