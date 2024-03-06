---
title : "Run the rule"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

1. On the AWS Config dashboard, select rules in the menu bar, then select add rule
   ![RunTheRule](../../image/3/3.3.1.png)

2. Add a new rule with the following parameters
   - Select rule type: Add AWS managed rule
   - AWS Managed Rules: search with keyword ec2-volume, then choose ec2-volume-inuse-check
   - click next 
   ![RunTheRule](../../image/3/3.3.2.png)


   - Evaluation mode:
     - Scope of changes: All changes
   - Parameters: click remove
   - Keep the remaining parameters as default, click next
   ![RunTheRule](../../image/3/3.3.3.png)


   - Review again and click save
   ![RunTheRule](../../image/3/3.3.4.png)


3. Return to the Rules page, click on the name of the newly created rule to see details
   ![RunTheRule](../../image/3/3.3.5.png)


4. Check the volume in the Resources in scope section
   ![RunTheRule](../../image/3/3.3.6.png)



5.  Compare with volumes in EC2
   ![RunTheRule](../../image/3/3.3.7.png)
  

{{% notice  note %}}
So we have created an AWS config with the rule that the ec2 volume is in use, any volume that is not used/attached to ec2 will be shown in the list Resources in scope as Noncompliant.
{{% /notice %}}
