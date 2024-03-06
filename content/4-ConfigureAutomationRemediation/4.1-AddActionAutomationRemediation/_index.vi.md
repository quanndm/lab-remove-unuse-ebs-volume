---
title : "Thêm automation remediation action"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

1. Ở trang AWS config, chọn Rule ở thanh menu
   - Filter by compliance status: Chọn Noncompliant
   - chọn ec2-volume-inuse-check
   - click Actions
   - click Manage remediation
   ![AddAction](/images/4/4.1.1.png)

2. Ở trang Edit: Remediation action
   - click chọn Automatic remediation
   - Retries in: 5
   - Seconds: 300
   - Choose remediation action: search với từ khoá AWSConfigRemediation-DeleteUnusedEBSVolume, sau đó click chọn
   ![AddAction](/images/4/4.1.2.png)


   - Rate limits:
     - Concurrent Execution Rate: 2
     - Error Rate: 5
   - Resource ID parameter: VolumeId
   - Parameters:
      - CreateSnapshot: true
      - AutomationAssumeRole: ARN of AssumeRole
      ![AddAction](/images/4/4.1.3.png)
      

      - Sau đó nhấn vào save changes
   ![AddAction](/images/4/4.1.4.png)

   - Save thành công
   ![AddAction](/images/4/4.1.5.png)




