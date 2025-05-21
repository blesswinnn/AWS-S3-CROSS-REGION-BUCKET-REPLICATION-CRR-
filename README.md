# AWS-S3-CROSS-REGION-BUCKET-REPLICATION-CRR

## 🚀 Overview

This project demonstrates how to **replicate objects from one S3 bucket to another across AWS regions** using **S3 Cross-Region Replication (CRR)**. It's essential for:
- Disaster recovery
- Data locality compliance
- Reduced latency for global users
- Backup and resilience strategies

# 🧠 Key Concepts
## ✅ What is S3 Cross-Region Replication (CRR)?
  - S3 CRR allows automatic, asynchronous copying of objects across S3 buckets in different AWS regions. This is useful when you want to:
  - Keep backups in another region
  - Serve content faster to users globally

## 🔐 Prerequisites
- Source and destination buckets must have versioning enabled
- IAM roles and policies must allow s3:ReplicateObject, s3:ReplicateDelete, etc.
- KMS keys should be used if encryption is enabled

## ⚙️ How It Works
- Create source and destination buckets in different AWS regions
- Enable versioning on both buckets
- Define a replication rule on the source bucket
- Create an IAM role that S3 uses to replicate objects
- Upload an object to the source bucket and observe it being replicated
- Optional: Use KMS for encryption and advanced bucket policies for fine-grained control.

# 🌐 Architecture

- Region A: Source Bucket

- Region B: Destination Bucket

- IAM Role with replication permissions

- Optional: CloudWatch for monitoring

# 📌 Features
- ✅ Auto-provisioned IAM Role for replication

- ✅ Cross-region support with customizable regions

- ✅ KMS encryption support

#WORKFLOW:

# create bucket in oregon reagion:

![image](https://github.com/user-attachments/assets/b7a2d5df-1280-4d04-832e-9fe115298a4c)

# create bucket in virgina reagion:

![image](https://github.com/user-attachments/assets/f5f662f5-eae0-4813-8220-cdfa835b83a7)

# UPLOAD OBJECT IN SOURCE BUCKET :

![image](https://github.com/user-attachments/assets/c91fa79d-bbf4-45a1-b927-7d9cce59673c)

# currently destination bucket is empty:

![image](https://github.com/user-attachments/assets/2da85f74-9020-4e6e-93a1-5159c1d082f1)

# under management tab create replication rule:

![image](https://github.com/user-attachments/assets/662c3018-7418-40d6-b5d8-bd1777a67215)

# ENABLE BUCKET VERSION FOR BOTH BUCKETS

![image](https://github.com/user-attachments/assets/eab71c58-c21d-4352-accc-c1e6ef6a4655)

# replication role creation:
![image](https://github.com/user-attachments/assets/69b5d112-3a20-4478-ae62-e5bfc1e54ad8)

![image](https://github.com/user-attachments/assets/513ac0b5-b1dc-4903-affb-6c4136945bc1)
![image](https://github.com/user-attachments/assets/f23a7deb-75c2-4429-b505-99e9a5f6d927)

![image](https://github.com/user-attachments/assets/5b6604ab-3674-4665-b285-63c8a38ba52f)

# batch operation job creation :

![image](https://github.com/user-attachments/assets/268a5d14-96e1-469b-b435-fb28a3e211ee)
![image](https://github.com/user-attachments/assets/6f7387e2-1129-4729-abee-8e8af7bbc563)
 
# virginia bucket has been populated with replicated data:

![image](https://github.com/user-attachments/assets/4df27d0d-5a9d-4f21-9c86-ff62eb771401)

# DELETE YOUR RESOURCES

