<div align="center">

<img src="https://img.shields.io/badge/AWS-Cloud%20Services-%23232F3E?style=for-the-badge" alt="AWS"/>
<br>
<h1>☁️🚀 AWS Quick Reference 🚀☁️</h1>
</div>

---

## 🌐 Type of Cloud
- ☁️ Public
- 🔒 Private
- 🌗 Hybrid

---

## 🛡️ AWS IAM
**Identity and Access Management** (Authentication & Authorization)

- 👤 Users
- 📜 Policies
- 👥 Groups
- 🎭 Roles (Temporary Purpose)

---

## 🖥️ AWS EC2 (Elastic Cloud Compute)

**Problems:**
- ⏰ Timely Upgrade
- 🛡️ Security Issues
- ⚠️ Server Goes Down

### 🖥️ Types of EC2 Instances
- 🟦 General Purpose
- 🟥 Compute Optimized
- 🟩 Memory Optimized
- 🟨 Storage Optimized
- 🟪 Accelerated Optimized

**To change permission of the file:**
```bash
chmod 600
```
- `chmod`: change mode  
- `6`: read & write for owner  
- `0`: no permissions for group/others

**For SSH:**
```bash
ssh -i "key" ubuntu@"public_ip"
```

**For Update:**
```bash
sudo apt update
```

**Switch to Root User:**
```bash
sudo su -
```

**For Logout:**
```bash
logout
```

**For Update in Root User:**
```bash
apt update
```

---

## 🕸️ VPC (Virtual Private Cloud)
A secure, isolated private cloud hosted within a public cloud.

- 📶 Subnets: Range of IPs in your VPC (must reside in single AZ)
- 🚀 Deploy AWS resources after adding subnets

**Request Route:**  
🌐 Internet Gateway → 🟦 Public Subnet → 🛡️ Load Balancer → 🛣️ Route Table → 🔒 Security Group → 💻 Application

- 🎭 NAT: Masks outgoing IP address
- 📊 VPC Flow Log: Security group at EC2 level
  - 🔼 Inbound traffic
  - 🔽 Outbound traffic

_Default Security Group:_  
✅ Allows all outbound except port 25 (mail)  
⛔ Denies all inbound

**NACL (Network Access Control List):**
- 🛡️ Optional firewall at subnet level (first layer of defense)

---

## 🌍 Route 53
**DNS (Domain Name Service)**  
- 🌐 Maps domain name with IP address

- 📝 Domain Registration
- 🔄 DNS Routing
- ❤️‍🩹 Health Checking: Automated requests to verify resource availability

_Generally, DNS maps to Load Balancer IP_

---

## 🛡️ Accessing Private Subnet
- 🕵️‍♂️ Use "Bastion-Host" to connect

---

## ⚖️ Load Balancer Types
- 📱 Application Load Balancer
- 🌐 Network Load Balancer
- 🚪 Gateway Load Balancer

---

## 🔁 NAT Gateway (Network Address Translation)
Allows private subnet instances to connect outward only.

- 🤝 VPC Peering: Communicate between different private subnet instances
- 🚦 Strict Network Access: NACL at subnet level
- 🛣️ VPC Endpoint: Securely access AWS services within VPC (S3, DynamoDB)

---

## 🗄️ AWS S3 (Simple Storage Service)

**Advantages:**
- 📶 Availability & Durability
- 📈 Scalability
- 🛡️ Security
- 💸 Cost Effective
- ⚡ Performance

**Security:**
- 🪣 Bucket Policies
- 🔒 Access Control
- 🗝️ Encryption

**Storage Classes:**
- 🟦 S3 Standard (least access time)
- 🟩 S3 Standard-IA
- 🟨 One Zone-IA
- ❄️ S3 Glacier
- 🚀 S3 Glacier Instant Retrieval
- 🔄 S3 Glacier Flexible Retrieval
- 🕳️ S3 Glacier Deep Archive
- 🏢 S3 Outposts
- 🧠 S3 Intelligent Tiering

---

## 🏗️ IAC (Infrastructure as Code)
- 🐍 AWS CLI (Python Utility)
- 🌱 Terraform
- 🏗️ Cloud Formation
- 🛠️ CDK

### AWS CLI (Quick Actions)
```bash
aws configure
```
```bash
aws s3 ls
```

---

## 🏗️ AWS CFT (Cloud Formation Template, IaC)
- Build large infrastructure in AWS
- Middleman between cloud and user
- Supports JSON & YAML templates
- Converts templates to API calls

**Template Style:**
- 📝 Declarative
- 🗂️ Versioned

**CFT Job:**
- 🏗️ Creating Infra
- 🕵️ Drift Detection (detect config changes outside CloudFormation)

---

## 🔗 AWS DevOps Services
- 🗃️ AWS Code Commit
- 🛠️ AWS Code Pipeline
- 🏗️ AWS CodeBuild
- 🚀 AWS Code Deploy

---

<div align="center">
  <sub>
    Made with ❤️ by taps453
  </sub>
</div>
