# Ops-to-DevOps Journey

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![GitHub Repo Size](https://img.shields.io/github/repo-size/cb0n3y/ops-to-devops-journey)
![Last Commit](https://img.shields.io/github/last-commit/cb0n3y/ops-to-devops-journey)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/cb0n3y/ops-to-devops-journey/ci.yml?label=CI%2FCD)

Welcome to my **Ops-to-DevOps Journey** portfolio. This repository serves as the **central roadmap** of my DevOps learning path, documenting my progression from Linux fundamentals to advanced CI/CD, containerization, cloud, and GitOps workflows.

All technical work is organized in **satellite repositories**, while this repo remains **clean, professional, and interview-ready**, showing curated evidence of my DevOps skills.

---

## 🔹 Roadmap Overview

This journey is structured in stages, reflecting real-world DevOps practices:

### **1️⃣ Foundations**
- **Linux & Networking** → [Linux & Networking](https://github.com/cb0n3y/linux-portfolio)
- **Application Basics** → curated docs & examples
- **Git & Version Control** → [Git Portfolio](https://github.com/cb0n3y/git-portfolio)

### **2️⃣ Automation & Scripting**
- **Bash Scripting** → [Bash Scripting Repo](https://github.com/cb0n3y/bash-scripting)
- **Python Scripting** → [Python Scripting Repo](https://github.com/cb0n3y/python-scripting)
- **AI-assisted Scripting** → optional examples

### **3️⃣ Infrastructure & Environment Setup**
- **Vagrant & Linux Servers** → [Vagrant Environments](https://github.com/cb0n3y/vagrant-environments)
- **Terraform (IaC)** → [Terraform Modules](https://github.com/cb0n3y/terraform-modules)
- **Ansible (Configuration Management)** → [Ansible Playbooks](https://github.com/cb0n3y/ansible-playbooks)

### **4️⃣ Containers & Orchestration**
- **Docker** → [Docker Examples](https://github.com/cb0n3y/docker-examples)
- **Kubernetes & Helm** → [Kubernetes Workflows](https://github.com/cb0n3y/kubernetes-workflows)
- **App Deployment** → deployment examples

### **5️⃣ CI/CD & DevOps Automation**
- **Jenkins Pipelines** → [Jenkins Pipelines](https://github.com/cb0n3y/jenkins-pipelines)
- **GitHub Actions** → [GitHub Actions Examples](https://github.com/cb0n3y/github-actions-portfolio)
- **GitLab CI/CD** → optional

### **6️⃣ Cloud & Projects**
- **AWS & Lift-and-Shift** → [AWS Projects](https://github.com/cb0n3y/aws-projects)
- **GCP Projects** → [GCP Projects](https://github.com/cb0n3y/gcp-projects)

### **7️⃣ Monitoring & Security**
- **Prometheus & Grafana** → [Monitoring & Observability](https://github.com/cb0n3y/prometheus-grafana)
- **Security & Best Practices** → curated docs & SECURITY.md

### **8️⃣ GitOps & Advanced Practices**
- **GitOps Workflows** → [GitOps Examples](https://github.com/cb0n3y/gitops-examples)
- **ArgoCD, FluxCD, Helm** → future satellite repos

---

## 📌 Why This Structure

- **Clean main repo:** focuses on roadmap, links, screenshots, and professional presentation
- **Satellite repos:** contain full implementations, pipelines, scripts, IaC, and project examples
- **Private bootcamp materials:** remain personal learning labs; only selected outcomes are showcased

This approach demonstrates **maturity, organization, and real-world DevOps workflow awareness**.

---

## 📑 How to Explore

1. Start with the **Foundations** stage (Linux, Git)
2. Progress through **Automation, Infrastructure, Containers, CI/CD**
3. Explore **Cloud, Monitoring, and GitOps** for advanced scenarios
4. Each link points to a **satellite repo with detailed examples**

> ⚠️ This portfolio is a **living document** — stages are continuously updated as I learn new tools and practices.

---

## 🛠 CI Pipeline

A minimal CI workflow ensures code consistency:

- **Lint trailing whitespace**
- (Each satellite repo has its own extended CI/CD pipelines)

```yaml
name: CI Pipeline
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
jobs:
  lint-trailing:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Check for trailing whitespace
        run: |
          if grep -rI --include '*.yml' --include '*.md' '[[:space:]]$' ./; then
            echo "Trailing whitespace found!"
            exit 1
          else
            echo "No trailing whitespace."
          fi
```

## 📄 License

This project is licensed under the [MIT License](LICENSE).
