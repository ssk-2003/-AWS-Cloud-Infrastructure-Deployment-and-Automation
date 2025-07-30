# AWS Cloud Infrastructure Deployment and Automation

This project demonstrates how to deploy a scalable, secure, and resilient cloud infrastructure using Amazon Web Services (AWS). It covers the full setup process, from creating a VPC to configuring EC2, RDS, ALB, CloudFront, and Route 53.

📄 **Author**: Satish Kumar  
📘 **Report**: [AWS Project Full Report by Satish Kumar.pdf](AWS%20Project%20Full%20Report%20by%20Satish%20Kumar.pdf)

---

## 🔧 Project Overview

The project includes:

1. **VPC Setup**  
   - Custom VPC with subnets for security and resource isolation

2. **S3 Bucket**  
   - File and media storage

3. **Elastic File System (EFS)**  
   - Shared file system across EC2 instances

4. **EC2 Instances with NGINX**  
   - Hosting a basic static site using a custom index.html

5. **RDS (Relational Database Service)**  
   - MySQL database setup with optional read replicas

6. **Application Load Balancer (ALB)**  
   - Distributing traffic across EC2 instances

7. **Auto Scaling Group (ASG)**  
   - Automatically scales EC2 instances based on demand

8. **CloudFront CDN**  
   - Faster content delivery through edge caching

9. **Route 53 DNS + ACM (SSL)**  
   - Secure HTTPS with DNS-based routing

---

## 🚀 AWS Infrastructure Deployment Steps (Flowchart)
```
[Start]
  │
  ├── 1️⃣ VPC Setup
  │     └─ Create VPC, Public & Private Subnets, IGW, Route Tables
  │
  ├── 2️⃣ S3 Bucket
  │     └─ Store static assets (e.g., images, backups)
  │
  ├── 3️⃣ EFS (Elastic File System)
  │     └─ Create & mount across EC2 in private subnets
  │
  ├── 4️⃣ EC2 with NGINX
  │     └─ Launch Ubuntu EC2, install NGINX, mount EFS, deploy app
  │
  ├── 5️⃣ RDS (MySQL)
  │     └─ Launch DB in private subnet, configure with security groups
  │
  ├── 6️⃣ Application Load Balancer (ALB)
  │     └─ Create Target Group, attach EC2s, set HTTP/HTTPS listeners
  │
  ├── 7️⃣ Auto Scaling Group (ASG)
  │     └─ Define launch template & scaling policies (CPU/traffic)
  │
  ├── 8️⃣ CloudFront CDN
  │     └─ Cache from ALB/S3, enable SSL for faster global access
  │
  ├── 9️⃣ Route 53 + ACM (SSL)
  │     └─ Connect domain, add DNS records, apply SSL certificate
  │
  └── ✅ Done! Production-ready AWS deployment.
```
---

## 🛠 Technologies Used

- Amazon VPC  
- Amazon S3  
- Amazon EC2 (Ubuntu)  
- Amazon EFS  
- Amazon RDS (MySQL)  
- AWS ALB & ASG  
- AWS CloudFront  
- AWS Route 53  
- AWS Certificate Manager (ACM)  
- NGINX web server  
- MySQL client

---

## 🗂 File List

- `AWS Project Full Report by Satish Kumar.pdf`: Full project documentation and step-by-step setup guide.

---

## 🌐 Final Workflow Diagram (Conceptual)

User → Route 53 → CloudFront → ALB → EC2 → RDS


---
🔄 Explanation of Each Step
👤 User
→ The end-user accessing your application via a web browser.

🌐 Route 53
→ DNS service that routes user traffic to the correct resource (your domain like satish.shop points to CloudFront or ALB).

⚡ CloudFront (CDN)
→ Delivers cached content (like images, static files) quickly from edge locations. Improves performance and reduces latency.

🔀 ALB (Application Load Balancer)
→ Distributes incoming requests across EC2 instances. It can also handle HTTPS termination using ACM SSL certificates.

💻 EC2 (with NGINX)
→ Your web server hosting the application, pulling shared content from EFS and possibly interacting with RDS.

🛢️ RDS (MySQL)
→ Your backend database storing dynamic content, user data, etc.

---

## 📝 Notes

- The report includes actual AWS Console steps and CLI commands.
- Designed for practical deployment of a static or dynamic web application.

---

## 📬 Contact

For any queries or feedback:  
📧 satishkumarcse2003@gmail.com
