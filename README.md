# 🍔 Automated CI/CD Pipeline for Online Food Delivery Application

## 📌 Project Overview

This project demonstrates an end-to-end **DevOps CI/CD pipeline** for deploying a containerized Online Food Delivery web application using the following DevOps tools:

- Git & GitHub
- Docker
- Jenkins
- Ansible
- Terraform
- Kubernetes

The objective is to automate the build and deployment process while demonstrating the integration of multiple DevOps tools.

---

# 🏗️ Infrastructure Architecture

```
                     GitHub
                        │
                        ▼
              Jenkins (devops-master)
          (Pipeline Script from SCM)
                        │
                        ▼
              build-agent (Docker)
        Build Docker Image & Push Image
                        │
                        ▼
                  Docker Hub
                        │
                        ▼
            Kubernetes (kube-server)
         Deploy Application using YAML
                        │
                        ▼
                  Browser Access
```

---

# 🖥️ Infrastructure

| Machine | Purpose |
|----------|----------|
| devops-master | Jenkins, Ansible, Terraform |
| build-agent | Docker Build Agent |
| kube-server | Kubernetes Single Node Cluster |

---

# 🛠️ Technologies Used

- Git
- GitHub
- Jenkins
- Docker
- Docker Hub
- Ansible
- Terraform
- Kubernetes
- Ubuntu 24.04 LTS
- AWS EC2

---

# 📂 Project Structure

```
food-delivery-app/
│
├── Dockerfile
├── Jenkinsfile
├── index.html
│
├── ansible/
│   ├── inventory
│   └── playbook.yml
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
└── kubernetes/
    ├── deployment.yaml
    └── service.yaml
```

---

# ⚙️ DevOps Workflow

## Step 1: Source Code Management

- Create Git Repository
- Push project to GitHub
- Version Control using Git

---

## Step 2: Configuration Management

Using **Ansible**

Configured:

- Jenkins Installation
- Java Installation
- Docker Installation
- Docker Service
- Jenkins Service

---

## Step 3: CI Pipeline

Using **Jenkins**

Pipeline Stages

- Checkout Source Code
- Build Docker Image
- Run Docker Container

---

## Step 4: Infrastructure Provisioning

Using **Terraform**

Provisioned infrastructure for:

- Kubernetes Server

---

## Step 5: Containerization

Using **Docker**

Docker Image built using

```
Dockerfile
```

Docker image pushed to Docker Hub.

---

## Step 6: Kubernetes Deployment

Using

- Deployment
- Service

Application deployed into Kubernetes Cluster.

---

# 🚀 Jenkins Pipeline

```
GitHub
   │
   ▼
Checkout Source Code
   │
   ▼
Build Docker Image
   │
   ▼
Push Docker Image
   │
   ▼
Deploy to Kubernetes
```

---

# ☸️ Kubernetes Deployment

Deployment creates

- Deployment
- ReplicaSet
- Pod

Service exposes application using

- NodePort

---

# 📋 Commands Used

## Git

```bash
git init
git add .
git commit -m "Initial Commit"
git remote add origin <repository-url>
git push -u origin main
```

---

## Docker

```bash
docker build -t food-delivery-app .
docker tag food-delivery-app <dockerhub-username>/food-delivery-app:latest
docker login
docker push <dockerhub-username>/food-delivery-app:latest
```

---

## Jenkins

Pipeline configured using

```
Pipeline Script from SCM
```

Repository

```
GitHub Repository
```

Script Path

```
Jenkinsfile
```

---

## Terraform

```bash
terraform init
terraform validate
terraform plan
terraform apply
```

---

## Kubernetes

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get svc
```

---

# 📷 Output

Application successfully deployed.

```
PRT - Food Delivery App Deployment Successful
```

Accessible through

```
http://<Node-IP>:30080
```

---

# 📊 CI/CD Flow

```
Developer
      │
      ▼
GitHub Repository
      │
      ▼
Jenkins Pipeline
      │
      ▼
Checkout Source Code
      │
      ▼
Docker Build
      │
      ▼
Docker Hub
      │
      ▼
Kubernetes Deployment
      │
      ▼
NodePort Service
      │
      ▼
Browser
```

---

# 🎯 Learning Outcomes

- Git Version Control
- Jenkins Pipeline
- Docker Image Creation
- Docker Hub Integration
- Ansible Automation
- Terraform Provisioning
- Kubernetes Deployment
- Complete CI/CD Pipeline

---

# 👨‍💻 Author

**Rakesh S**

Senior Software Engineer

GitHub: https://github.com/RS-cloud-intellipaat

---

# ⭐ Project Status

✅ Completed Successfully

```
Application Deployment Successful
```
