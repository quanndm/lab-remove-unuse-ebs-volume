---
title : "Add the automatic remediation action"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

1. On the AWS config page, select Rule in the menu bar
   - Filter by compliance status: Choose Noncompliant
   - Choose ec2-volume-inuse-check
   - click Actions
   - click Manage remediation
   ![AddAction](../../image/4/4.1.1.png)

2. On Edit: Remediation action page
   - click Automatic remediation
   - Retries in: 5
   - Seconds: 300
   - Choose remediation action: Search with the keyword AWSConfigRemediation-DeleteUnusedEBSVolume, then click to select it
   ![AddAction](../../image/4/4.1.2.png)


   - Rate limits:
     - Concurrent Execution Rate: 2
     - Error Rate: 5
   - Resource ID parameter: VolumeId
   - Parameters:
      - CreateSnapshot: true
      - AutomationAssumeRole: ARN of AssumeRole
      ![AddAction](../../image/4/4.1.3.png)
      

      - Sau đó nhấn vào save changes
   ![AddAction](../../image/4/4.1.4.png)

   - Save successfully
   ![AddAction](../../image/4/4.1.5.png)




