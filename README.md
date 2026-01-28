# AWS Networks – Virtual Private Cloud (VPC)

This repository documents my hands-on learning and implementation of **AWS networking fundamentals** through the **AWS Networks – VPC project series** by **NextWork**.

The goal of this series is to understand how AWS Virtual Private Clouds (VPCs) work by building, securing, and connecting networks step by step using real AWS services.

---

## 📌 What This Series Covers

Through this project series, I learned how to:

- Design and create a Virtual Private Cloud (VPC)
- Configure public and private subnets
- Control traffic using route tables, internet gateways, and NAT
- Secure networks with Security Groups and Network ACLs
- Launch AWS resources inside a VPC
- Test and troubleshoot network connectivity
- Connect VPCs using VPC Peering
- Monitor traffic using VPC Flow Logs
- Access AWS services privately using VPC Endpoints

---

## 🗂 Repository Structure

aws-networks-vpc/
├── 01-create-vpc/
├── 02-traffic-flow-and-security/
├── 03-create-private-subnet/
├── 04-launch-vpc-resources/
├── 05-test-vpc-connectivity/
├── 06-vpc-peering/
├── 07-vpc-flow-logs/
├── 08-access-s3-from-vpc/
├── 09-vpc-endpoints/
└── README.md

Each folder represents one project and contains notes, screenshots, and configuration details related to that step.

---

## 📘 Project Breakdown

### 1️⃣ Create a VPC
- Created a custom VPC
- Defined CIDR blocks
- Created a public subnet
- Attached an Internet Gateway
- Associated route tables

### 2️⃣ Traffic Flow & Security
- Learned how traffic flows within a VPC
- Configured route tables
- Set up Security Groups
- Implemented Network ACLs

### 3️⃣ Create a Private Subnet
- Created private subnets
- Understood isolation from the internet
- Learned when and why private subnets are used

### 4️⃣ Launch Resources in a VPC
- Launched EC2 instances in public and private subnets
- Associated security groups
- Reviewed networking behavior

### 5️⃣ Test VPC Connectivity
- Tested connectivity between instances
- Verified internet access
- Troubleshot routing and security issues

### 6️⃣ VPC Peering
- Connected two VPCs using VPC peering
- Updated route tables
- Verified cross-VPC communication

### 7️⃣ VPC Flow Logs
- Enabled VPC Flow Logs
- Captured network traffic data
- Learned basic traffic analysis

### 8️⃣ Access S3 from a VPC
- Accessed Amazon S3 without internet access
- Used Gateway VPC Endpoints
- Improved security and performance

### 9️⃣ VPC Endpoints
- Implemented VPC endpoints
- Learned differences between Gateway and Interface endpoints
- Enabled private AWS service access

---

## 🎯 Learning Outcomes

By completing this series, I gained:

- Strong understanding of AWS networking concepts
- Hands-on experience with real AWS infrastructure
- Practical skills relevant to cloud engineering and AWS certifications
- Confidence in designing secure and scalable VPC architectures

---

## 🛠 Tools & Services Used

- Amazon VPC
- EC2
- Internet Gateway
- Route Tables
- Security Groups & Network ACLs
- VPC Peering
- VPC Flow Logs
- VPC Endpoints
- AWS Management Console

---

## ⚠️ Cost Awareness

Some services (such as NAT Gateways and VPC Flow Logs) may incur AWS charges.  
All resources were deleted after completing each project to avoid unnecessary costs.

---

## 📚 Reference

- **NextWork – AWS Networks: VPC Project Series**
- **AWS Official Documentation**

---

## ✍️ Author

**Naeem Noor**  
Cloud & IT Enthusiast | AWS Learner  

---

⭐ If you find this repository helpful, feel free to star it!
