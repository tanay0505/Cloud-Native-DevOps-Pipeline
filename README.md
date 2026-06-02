# Cloud-Native DevOps Pipeline

## Overview

This project demonstrates an end-to-end DevOps workflow for deploying and managing a cloud-native microservices application on AWS. The focus of this project is on infrastructure automation, container orchestration, CI/CD implementation, GitOps practices, and observability.

The application consists of multiple containerized services deployed on Amazon EKS, with infrastructure provisioned using Terraform and deployments automated through GitHub Actions and ArgoCD.

---

## Architecture

```text
Developer
    ↓
GitHub Repository
    ↓
GitHub Actions
    ↓
Docker Build
    ↓
Amazon ECR
    ↓
ArgoCD (GitOps)
    ↓
Amazon EKS
    ↓
Microservices
    ↓
Prometheus & Grafana
```
---

## Key Features

- Infrastructure provisioning using Terraform modules
- Containerized microservices deployment with Docker
- Kubernetes orchestration on Amazon EKS
- Automated CI/CD pipelines using GitHub Actions
- GitOps-based deployment strategy with ArgoCD
- Centralized monitoring using Prometheus and Grafana
- Scalable and production-style cloud architecture

---

## Project Structure

```text
projects/
├── Infrastructure/        # Terraform configuration
├── boutique-microservices/ # Application services
├── aiops-assistant/       # Optional AIOps components
│
gitops/
├── k8s/                   # Kubernetes manifests
├── argo-cd.yml            # ArgoCD application
└── kustomization.yml      # Kustomize configuration
│
.github/
└── workflows/             # CI/CD pipeline
```

---

## CI/CD Workflow

1. Source code is pushed to GitHub.
2. GitHub Actions builds Docker images.
3. Images are pushed to Amazon ECR.
4. Kubernetes manifests are updated.
5. ArgoCD detects Git changes.
6. Changes are automatically synchronized to EKS.

---

## Monitoring & Observability

The platform includes:

- Prometheus for metrics collection
- Grafana dashboards for visualization
- Centralized logging for troubleshooting
- Health monitoring for deployed services

---

## Learning Outcomes

Through this project, I gained hands-on experience with:

- Terraform-based Infrastructure as Code
- Kubernetes deployment and management
- Amazon EKS administration
- Docker containerization
- GitOps workflows using ArgoCD
- CI/CD automation using GitHub Actions
- Monitoring and observability practices
- Cloud-native application deployment patterns

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Application | React, Node.js, PostgreSQL |
| Containers | Docker, Docker Compose |
| Orchestration | Kubernetes (AWS EKS) |
| Infrastructure | Terraform |
| CI/CD | GitHub Actions |
| GitOps | ArgoCD + Kustomize |
| Monitoring | Prometheus + Grafana |

---

## Disclaimer

The application source code used in this project is based on an existing microservices implementation. My primary contribution focused on the DevOps aspects including infrastructure provisioning, containerization, Kubernetes deployment, CI/CD automation, GitOps workflows, and observability setup.
