# Serverless-Security-Remediation
# 🛡️ AWS S3 Bucket Guardian

An automated, serverless security remediation system that monitors AWS S3 buckets and automatically reverts "Public Access" settings to "Private" if they are changed.

## 🚀 Overview
In cloud security, misconfigured S3 buckets are a leading cause of data breaches. This project implements a **Self-Healing Infrastructure** concept where any attempt to make a bucket public is immediately detected and corrected without human intervention.

## 🏗️ Architecture
The system follows an event-driven flow:
1. **User/Attacker** modifies S3 Bucket Public Access settings.
2. **AWS CloudTrail** logs the `PutBucketPublicAccessBlock` API call.
3. **Amazon EventBridge** matches the event and triggers a Lambda function.
4. **AWS Lambda (Python/Boto3)** resets the bucket's "Block Public Access" settings to `True`.
5. **Amazon SNS** sends an email notification to the administrator with the remediation details.



## 🛠️ Tech Stack
- **Cloud Provider:** Amazon Web Services (AWS)
- **Services:** S3, Lambda, EventBridge, CloudTrail, SNS, IAM
- **Language:** Python 3.12 (Boto3 SDK)

## 📸 Screenshots
*(Add your screenshots here for better visibility)*
 [https://github.com/cit-24-01-0532-cyber/Serverless-Security-Remediation/blob/main/Screenshot%202026-05-10%20075551.png]
 [https://github.com/cit-24-01-0532-cyber/Serverless-Security-Remediation/blob/main/Screenshot%202026-05-10%20075617.png]
 [https://github.com/cit-24-01-0532-cyber/Serverless-Security-Remediation/blob/main/Screenshot%202026-05-10%20075649.png]

## 📝 Key Learnings
- Configuring **CloudTrail** for account-wide event monitoring.
- Writing **EventBridge Rules** to capture specific API-level changes.
- Using **Boto3** to programmatically enforce security compliance.
- Understanding **Auto-Remediation** patterns in DevSecOps.

---
Created by [Isara Perera-2026]
