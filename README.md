# Deployment-of-Java-Application-Using-GitHub-Actions-Docker-Amazon-ECR-and-Amazon-ECS

---

## 🧠 Introduction

This project demonstrates a **fully automated CI/CD pipeline** to deploy a Java application using modern DevOps tools.

The pipeline automates:
- Build
- Containerization
- Image storage
- Deployment

👉 Eliminates manual work and ensures fast, reliable releases.

---

## 🛠️ Tools Used

- **GitHub** – Source code management  
- **GitHub Actions** – CI/CD automation  
- **Docker** – Containerization  
- **Amazon ECR** – Image repository  
- **Amazon ECS (Fargate)** – Container deployment  
- **IAM** – Authentication & authorization  
- **CloudWatch** – Logging & monitoring  

---

## 🧱 Architecture Flow

Developer Push Code → GitHub  
→ GitHub Actions Pipeline  
→ Docker Image Build  
→ Push to Amazon ECR  
→ ECS Deployment  
→ Running Container  

---

## ⚙️ Step-by-Step Implementation

---

### 1️⃣ Create Amazon ECR

- Create private Docker repository  
- Name: `project-image-repo`  
- Used to store container images  

---

### 2️⃣ Create Amazon ECS Cluster

- Create ECS cluster using **Fargate**  
- Name: `projec-cluster`  

---

### 3️⃣ Create Task Definition

- Configure:
  - Container image  
  - CPU & Memory  
  - Port mapping  

---

### 4️⃣ Create ECS Service

- Create service to maintain running containers  
- Name: `project-task-definition-service`  

---

### 5️⃣ Create IAM Credentials

- Generate:
  - AWS Access Key  
  - AWS Secret Key  

---

### 6️⃣ Configure GitHub Repository

- Push source code to GitHub  
- Add **Dockerfile**  
- Create workflow file:
