# Secure Cloud-Hosted Web Application on AWS

## 📌 Project Level
Intermediate / Internship-Level Project

---

## 📖 Project Description
This project demonstrates the deployment of a secure cloud-hosted web application using Amazon Web Services (AWS).  
A simple web application was developed and hosted on an AWS EC2 Free Tier instance, following cloud security best practices.  
The project focuses on secure access, proper resource management, and cost optimization.

---

## 🎯 Objectives
- To understand cloud-based web application deployment
- To host a web application using AWS EC2
- To configure security using IAM and Security Groups
- To follow AWS Free Tier usage and avoid billing
- To document the deployment using GitHub

---

## 🛠️ Technologies & Services Used
- AWS EC2 (Free Tier)
- AWS IAM
- AWS Security Groups
- Apache Web Server
- HTML
- Git & GitHub

---

## 🧩 Project Architecture
User → Internet → Security Group (Firewall) → EC2 Instance → Web Application

---

## 🚀 Implementation Steps (AWS EC2 + Apache Web Hosting)

---

### ✅ Step 1 (Optional): Create an AWS IAM User (For Secure Access)

This step is optional.  
If you want secure access and want to avoid using the root account, you can create an IAM user.  
Otherwise, you can directly continue to **Step 2**.

1. Login to **AWS Management Console**
2. Go to: **IAM → Users → Add users**
3. Enter username (example: `ec2-admin-user`)
4. Enable:
   - ✅ AWS Management Console access
5. Set permissions:
   - Choose **Attach policies directly**
   - Attach:
     - ✅ `AdministratorAccess` (Full Admin Access)
6. Create the user and save login details

📌 After creating the IAM user, **logout from root** and login again using the IAM user you created.

---

### ✅ Step 2: Launch a Free Tier EC2 Instance

1. Login using the **IAM user** (if created in Step 1)
2. Go to: **EC2 → Instances → Launch Instance**
3. Enter instance name:
   - Example: `Apache-HTML-Server`
4. Select AMI:
   - ✅ Ubuntu (Recommended because it is user-friendly and commonly used)
5. Choose Instance Type:
   - ✅ `t2.micro` (Free Tier eligible)
6. Create a Key Pair:
   - Key pair name: `ec2-key`
   - Download `.pem` file safely

---

### ✅ Step 3: Configure Security Group Rules

Create a new security group and add these inbound rules:

| Type | Protocol | Port | Source |
|------|----------|------|--------|
| SSH  | TCP      | 22   | My IP (recommended) |
| HTTP | TCP      | 80   | Anywhere (0.0.0.0/0) |

📌 SSH should be restricted to your IP for security.  
HTTP should be public so the website can be accessed.

---

### ✅ Step 4: Run the EC2 Instance Setup Commands (Using Repo Script)

Instead of manually running separate commands, you can directly use the setup script already provided in this GitHub repository.

📌 The setup code is available inside the folder:

```text
ec2-setup/
```
This setup includes:

- Apache installation

- Starting and enabling the Apache service

- Deploying the HTML project files

- Required configuration for hosting the website

Run the commands from the terminal after connecting to your EC2 instance, as mentioned inside the `ec2-setup` folder.

---

### ✅ Step 5: Terminate AWS Resources (To Avoid Billing)

If you created this project only for learning/demo purpose, it is recommended to delete resources after testing to avoid billing.

1. Go to: EC2 → Instances

2. Select your instance

3. Click: Instance state → Terminate instance

4. Confirm termination

Also check and delete (if created):

  - Unused volumes

  - Elastic IP (if allocated)

---

## 🔐 Security Features
- IAM user used instead of root account
- SSH access restricted to specific IP
- Only required ports (22, 80) opened
- Basic monitoring enabled

---

## ✅ Conclusion
This project provided hands-on experience in cloud computing by deploying and securing a web application on AWS.  
It helped in understanding real-world cloud infrastructure, security practices, and cost control techniques.

---

## 🔮 Future Scope
- Add HTTPS using SSL/TLS
- Use Load Balancer for high availability
- Deploy a dynamic application with database
- Automate deployment using Infrastructure as Code

---

## 👤 Author
Umesh Saini  
AWS Project
2026
