---
title : "Configure AWS Config"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---


#### Configure AWS Config

In this section, we will begin configuring AWS Config, including creating roles for the automation runbook, starting the AWS Config recorder, and creating and launching the rules set up in AWS Config.

AWS Config recorder is used to store a history of configuration changes of one or more AWS resources. Convenient for auditing resource-related issues, combined with AWS Cloudtrail service

AWS Config Rule allows you to set rules based on AWS common or custom rules that you define. For example, you can ensure AWS EBS is encrypted, EC2 Instance is tagged, EIP is attached to EC2, check if EBS volume is in use, etc. Additionally, allow monitoring of AWS changes resource and provides a new dashboard to track.


#### Content

1. [Create role for Automation runbook](3.1-CreateRole/)
2. [Turn on AWS Config Recorder ](3.2-TurnOnAWSConfigRecorder/)
3. [Run the rule](3.3-RunTheRule/)
