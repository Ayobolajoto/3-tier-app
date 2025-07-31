#  3-Tier Web Application Infrastructure Automation

This project showcases the complete setup, automation, and deployment of a production-ready 3-tier web application using DevOps best practices. It includes infrastructure provisioning, containerization, orchestration, configuration management, and CI/CD integration — all built and deployed on AWS.

---

## Project Architecture

- **Frontend**: Nginx (or React, depending on the version)
- **Backend**: Node.js with Express.js
- **Database**: MongoDB
- **Infrastructure**: AWS EC2 (for all tiers)
- **Automation Tools**: Terraform, Docker, Docker Compose, Jenkins, Ansible, Kubernetes
- **CI/CD**: GitHub + Jenkins Pipelines

---

## Tools & Technologies

- **Infrastructure as Code**: Terraform
- **Configuration Management**: Ansible
- **Containerization**: Docker
- **Orchestration**: Docker Compose & Kubernetes
- **Version Control**: Git & GitHub
- **CI/CD**: Jenkins
- **OS Environment**: Ubuntu via WSL on Windows
- **Cloud**: Amazon Web Services (EC2 instances)

---

## Folder Structure

3-tier-app/
│
├── frontend/ # Frontend app source (Nginx/React)
├── backend/ # Node.js backend API with Express
├── terraform/ # Infrastructure provisioning code (AWS EC2 setup)
├── ansible/ # Configuration automation (to be implemented)
├── k8s/ # Kubernetes deployment configs (upcoming)
├── jenkins/ # Jenkins pipeline setup
└── docker-compose.yml # Local orchestration of the app

---

## Features Implemented

- ✅ Infrastructure provisioning using Terraform (3 EC2 instances for frontend, backend, and DB)
- ✅ Dockerized backend and frontend apps
- ✅ MongoDB database containerized with volume mapping
- ✅ Local development environment using Docker Compose
- ✅ Remote deployment to AWS via Terraform
- ✅ Cleanup of `.terraform` directory to reduce Git repo size
- ✅ Resolved GitHub push issues (large file filtering with `git filter-repo`)
- ⏳ Jenkins pipeline and Ansible configuration in progress

---

##  How to Run (Basic Workflow)

1. **Provision Infrastructure**

cd terraform

terraform init

terraform apply

2. Build and Run Locally (Optional)

docker-compose up --build

3. Access the App

Frontend: http://<public-ip>:3000

Backend API: http://<public-ip>:5000/api

MongoDB: running in container internally

4. CI/CD Pipeline

Jenkins pulls from GitHub and triggers build/test/deploy steps (coming next).

** Lessons & Challenges
Dealt with GitHub's 100MB file push limit by identifying and removing .terraform directory using git filter-repo

Managed Git authentication via personal access tokens (PAT)

Troubleshot MongoDB crash issues in Dockerized setup

Resolved PATH and environment issues inside WSL

Practiced backup and recovery before destructive Git operations

** Next Steps
 Automate provisioning with Ansible

 Set up full CI/CD pipeline using Jenkins

 Deploy app with Kubernetes on AWS

 Secure infrastructure with proper networking and IAM

** Author
Adedeji Olajoto
DevOps Engineer | Infrastructure Automation | Cloud Enthusiast
Nigeria
