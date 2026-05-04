# Devops-Internship-Projects
Collection of hands-on DevOps internship projects focused on AWS services, including secure application deployment, automated backup and recovery, and resilient data pipeline architecture using Docker

This repository contains my DevOps internship projects focused on deploying, securing, and managing cloud-based applications using AWS services.

👨‍💻 **Author:** Aniket Pawar  
🎓 **MCA Student | Cloud & DevOps Enthusiast**

---

## 📌 Projects Overview

This repository includes the following 3 projects:

- Java Application Deployment with Reverse Proxy on AWS  
- AWS Backup Plan for EC2 and RDS  
- Data Ingestion Pipeline (S3 → RDS with AWS Glue Fallback using Docker)  

---

## 🔹 Project 1: Java Application Deployment with Reverse Proxy on AWS

### 📖 Description
This project demonstrates deployment of a Java web application using a reverse proxy architecture on AWS.

### 🏗️ Architecture

User → Nginx Reverse Proxy (EC2) → Tomcat Server (EC2) → Amazon RDS (MySQL)


### ⚙️ Technologies Used
- Amazon EC2  
- Amazon RDS (MySQL)  
- Apache Tomcat  
- Nginx  
- Java (JSP)  
- Linux (Amazon Linux)  

### 🔄 Traffic Flow
- User request hits Nginx reverse proxy  
- Proxy forwards request to Tomcat server (port 8080)  
- Application processes data and stores in RDS  
- Response returned via proxy  

### ⚡ Key Features
- Secure backend (not publicly exposed)  
- Reverse proxy configuration  
- Database integration with RDS  

### 🛠️ Challenges & Solutions
- Database connection issue → Fixed using MySQL connector  
- Reverse proxy routing issue → Configured Nginx properly  
- Security issue → Restricted backend via security groups  

---

## 🔹 Project 2: AWS Backup Plan for EC2 and RDS

### 📖 Description
This project focuses on implementing automated backup and recovery using AWS Backup.

### 🎯 Objective
- Protect EC2 and RDS resources  
- Automate backups  
- Enable disaster recovery  

### 🏗️ Setup
- EC2 instance with Apache server  
- RDS MySQL database  
- Backup Vault: `project-backup-vault`  
- Backup Plan: Daily backups (Retention: 7 days)  

### ⚙️ Services Used
- Amazon EC2  
- Amazon RDS  
- AWS Backup  
- AWS IAM  

### ✅ Key Features
- Centralized backup management  
- Automated daily backups  
- Recovery point validation  

### 🔍 Outcome
- Successful backup jobs  
- Recovery points created and verified  

---

## 🔹 Project 3: Data Ingestion Pipeline (S3 → RDS with AWS Glue Fallback)

### 📖 Description
This project builds a fault-tolerant data pipeline using AWS and Docker.

### 🎯 Objective
- Read CSV data from S3  
- Insert into RDS  
- Use AWS Glue as fallback if RDS fails  

### 🏗️ Architecture

**Primary Flow:**
S3 → Dockerized Python App → Amazon RDS


**Fallback Flow:**
S3 → Dockerized Python App → AWS Glue

### ⚙️ Technologies Used
- Python  
- Pandas  
- Boto3  
- SQLAlchemy  
- Docker  
- AWS Services  

### 🔄 Workflow
- Upload CSV to S3  
- Python app reads data using Pandas  
- Insert into RDS  
- If failure → Switch to AWS Glue  

### ⚡ Key Features
- Fault-tolerant system  
- Automatic fallback mechanism  
- Docker containerization  

### 🛠️ Challenges
- AWS credential issues → Fixed using environment variables  
- RDS connectivity issues → Implemented fallback  
- IAM permissions → Proper role configuration  

---

## 📸 Screenshots
All project screenshots are included in the PDF file.

---

## 📄 Project Report
📎 Full detailed report available in this repository:  
`Devops Internship Projects.pdf`

---

## 🎯 Conclusion

These projects demonstrate hands-on experience in:

- Cloud deployment using AWS  
- Reverse proxy architecture  
- Backup & disaster recovery  
- Data pipeline development  
- Docker containerization  

---
