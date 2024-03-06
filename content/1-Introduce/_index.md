---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Overview
In this lab, you will practice deleting Amazon Elastic Block Store (Amazon EBS) volumes that are no longer in use, using AWS Config and AWS Systems Manager

Link AWS Prescriptive Guidance Patterns: [here](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/delete-unused-amazon-elastic-block-store-amazon-ebs-volumes-by-using-aws-config-and-aws-systems-manager.html)

When you complete this section, you will deploy the following infrastructure architecture:
![structure](/images/1/design.png)

- Steps:
    1. The AWS Config rule evaluates the EBS volumes.
    2. The rule returns a list of compliant and noncompliant resources. EBS volumes that are in the `available` state, which are unused volumes, are determined to be noncompliant.
    3. AWS Config automatically starts the Automation runbook.
    4. If configured, Systems Manager creates snapshots of the unused volumes before deleting them.
    5. Systems Manager deletes the unused EBS volumes.


##### AWS Config
- AWS Config is a fully managed service that provides you with an AWS resource inventory, configuration history, and configuration change notifications to enable security and governance. Config Rules enables you to create rules that automatically check the configuration of AWS resources recorded by AWS Config.
- Document: [here](https://aws.amazon.com/config)

##### AWS Systems Manager
- AWS Systems Manager is a management service that helps you automatically collect software inventory, apply OS patches, create system images, and configure Windows and Linux operating systems. These capabilities help you define and track system configurations, prevent drift, and maintain software compliance of your EC2 and on-premises configurations.
- Document: [here](https://aws.amazon.com/systems-manager)

#### Content

1. [Introduce](1-introduce/)
2. [Preparation](2-Preparation/)
3. [Configure the AWS Config](3-ConfigureAWSConfig/) 
4. [Configure automatic remediation](4-ConfigureAutomationRemediation/)
5. [Clean up resource](5-CleanUp/)
