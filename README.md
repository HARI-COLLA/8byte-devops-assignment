# 🚀 DevOps Intern Technical Assignment – 8byte AI

## 📌 Project Overview
This project demonstrates an end-to-end DevOps workflow by deploying a containerized Node.js application on AWS using **Infrastructure as Code (Terraform)** and **CI automation (GitHub Actions)**.

The application is packaged using Docker, infrastructure is provisioned on AWS using Terraform, and a CI pipeline validates Docker builds on every code push. The final application is publicly accessible via an EC2 public IP.

---

## 🧱 Technology Stack
- **Cloud Provider:** AWS  
- **Infrastructure as Code:** Terraform  
- **Containerization:** Docker  
- **CI/CD:** GitHub Actions  
- **Application Framework:** Node.js (Express)  
- **Operating System:** Ubuntu 22.04  
- **Instance Type:** t3.micro  

---

## 🏗️ Architecture Overview
**Workflow:**
1. Code push to GitHub  
2. GitHub Actions CI pipeline builds Docker image  
3. Infrastructure provisioned using Terraform  
4. Application deployed on AWS EC2  
5. Application accessed via public IP on port 3000  

---

## 📂 Project Structure
```text
8byte-devops-assignment/
│
├── app.js
├── package.json
├── Dockerfile
├── README.md
│
├── terraform/
│   ├── provider.tf
│   ├── variables.tf
│   ├── main.tf
│   ├── outputs.tf
│   └── terraform.tfvars
│
├── screenshots/
│   ├── terraform-apply.png
│   ├── ec2-running.png
│   ├── app-browser.png
│   └── github-actions.png
│
└── .github/
    └── workflows/
        └── ci.yml

'''

## ⚙️ Run Application Locally

npm install
node app.js

http://localhost:3000

# 🐳 Docker Setup

docker build -t 8byte-intern-app .
docker run -p 3000:3000 8byte-intern-app

# ☁️ Terraform Infrastructure Setup
terraform init
terraform plan
terraform apply

# 🚢 Deploy on EC2

ssh -i devops-key.pem ubuntu@<EC2_PUBLIC_IP>
git clone https://github.com/HARI-COLLA/8byte-devops-assignment.git
cd 8byte-devops-assignment
docker build -t 8byte-app .
docker run -d -p 3000:3000 8byte-app

# 🔁 CI/CD – GitHub Actions

Triggered on push to main
Builds Docker image automatically
Ensures build validation

# 🌐 Live Application
http://18.61.157.240:3000

## 📸 Screenshots

The following screenshots demonstrate successful completion of the assignment tasks.

### Terraform Apply Output
<img width="1472" height="1014" alt="Screenshot 2026-02-07 205337" src="https://github.com/user-attachments/assets/da7c0554-d2de-436a-82ae-3885ea11c657" />


### EC2 Instance Running
<img width="2848" height="1473" alt="Screenshot 2026-02-07 205520" src="https://github.com/user-attachments/assets/5d8fab04-195b-490c-8d5a-8ef2df05ecfc" />


### Application Working in Browser
<img width="2595" height="1396" alt="Screenshot 2026-02-07 211959" src="https://github.com/user-attachments/assets/fa955093-1466-4127-bfe3-f8f2a0158036" />


### GitHub Actions CI Pipeline
<img width="2567" height="1286" alt="Screenshot 2026-02-07 212503" src="https://github.com/user-attachments/assets/173cde03-ef17-408a-8564-7c01247a8b06" />


👤 Author
Mallangi Harinath Reddy
