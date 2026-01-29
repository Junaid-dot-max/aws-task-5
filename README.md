# AWS Task-5 – CI/CD Pipeline using AWS DevOps Services

## 📌 Task Description
Deploy a simple web application using **AWS CI/CD services** and automate the complete flow using **AWS CodePipeline**.  
The application must be accessible via a browser after deployment.

---

## 🛠️ Tech Stack Used
- AWS CodeCommit  
- AWS CodeBuild  
- AWS CodeDeploy  
- AWS CodePipeline  
- AWS EC2 (Amazon Linux 2)  
- Apache HTTP Server  

---

## 🏗️ Architecture Overview
Developer
|
v
AWS CodeCommit (Source)
|
v
AWS CodeBuild (Build)
|
v
AWS CodeDeploy (Deploy)

---

## 📂 Project Structure
aws-task-5-cicd/
├── index.html
├── buildspec.yml
├── appspec.yml
└── scripts/
└── install.sh

---

## 📄 File Description

### `index.html`
Simple static web page deployed on EC2 using Apache.

### `buildspec.yml`
Defines build instructions for AWS CodeBuild.

### `appspec.yml`
Defines deployment instructions for AWS CodeDeploy.

### `scripts/install.sh`
Installs and starts Apache web server on EC2.

---

## 🚀 Deployment Steps

### 1️⃣ EC2 Setup
- Launched Amazon Linux 2 EC2 instance
- Installed and started CodeDeploy agent
- Attached IAM role: `AmazonEC2RoleforAWSCodeDeploy`
- Opened ports:
  - SSH (22)
  - HTTP (80)
- Tagged EC2 instance:
- 
---

### 2️⃣ Source Stage – CodeCommit
- Created CodeCommit repository: `aws-task-5-cicd`
- Pushed application and configuration files

---

### 3️⃣ Build Stage – CodeBuild
- Created CodeBuild project
- Used `buildspec.yml`
- Generated build artifacts successfully

---

### 4️⃣ Deploy Stage – CodeDeploy
- Created CodeDeploy application
- Created deployment group targeting EC2 using tag
- Deployment type: In-place
- Successfully deployed application to EC2

---

### 5️⃣ Automation – CodePipeline
- Created CodePipeline with stages:
- Source (CodeCommit)
- Build (CodeBuild)
- Deploy (CodeDeploy)
- Pipeline triggers automatically on code changes

---

## 🌐 Application Access
After successful deployment, the application is accessible via browser:

### Output:
CI/CD Deployment Successful 🎉
AWS CodePipeline is working!

---

## 📸 Submission Proof
Screenshots included:
- CodeCommit repository
- CodeBuild successful build
- CodeDeploy successful deployment
- CodePipeline successful execution
- Browser output

---

## ✅ Final Outcome
- Fully automated CI/CD pipeline implemented
- Web application deployed successfully
- Task completed as per requirements

---

## 👤 Author
**Junaid**




v
EC2 Instance (Web Application)
