# kubeops-engine 🚀  
A fully automated DevOps pipeline integrating CI/CD and GitOps to deploy scalable cloud-native applications on AWS EKS.

---

## Overview
This project implements a **production-grade DevOps pipeline** for deploying a containerized web application on AWS EKS.  
It automates the entire build, test, deployment, and monitoring cycle — showcasing modern CI/CD and GitOps practices for scalable, reliable, and cloud-native systems.

---

## Features
- Automated Docker image builds and pushes via **GitHub Actions**
- Continuous Delivery with **ArgoCD** and **Helm**
- Multi-environment setup (**Dev**, **QA**, **Prod**)
- Infrastructure provisioning on **AWS EKS**
- Rollback and self-healing deployments through **GitOps**
- Modular, reusable Helm charts for environment-specific configuration

---

## Architecture
- **Containerization:** Dockerfile builds the application image  
- **CI Pipeline:** GitHub Actions automates build & push to DockerHub  
- **CD (GitOps):** ArgoCD syncs manifests to Kubernetes  
- **Infrastructure:** EKS cluster hosts multiple environments  
- **Helm Charts:** Manage configurations per environment  
- **Ingress + DNS:** NGINX Ingress Controller + AWS Load Balancer expose the app  

*(Architecture diagram to be added soon)*

---

## Tech Stack
| Category | Tool |
|-----------|------|
| Containerization | Docker |
| CI/CD | GitHub Actions, ArgoCD |
| Orchestration | Kubernetes (EKS) |
| Configuration | Helm |
| Cloud Provider | AWS |
| Monitoring | (optional) Prometheus / Grafana |

---

## Getting Started
To reproduce or test this pipeline locally:

```bash
# Clone the repository
git clone https://github.com/amanjotubhi/kubeops-engine.git
cd kubeops-engine

# Build the Docker image
docker build -t kubeops-engine .

# Deploy via Helm
helm install kubeops ./helm-chart

# Sync manifests with ArgoCD
# (to be added after ArgoCD setup)
