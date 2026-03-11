# DevSecOps CI/CD Pipeline Project

![DevSecOps](https://img.shields.io/badge/DevSecOps-CI%2FCD-blue)
![Jenkins](https://img.shields.io/badge/Jenkins-Automation-red)
![Docker](https://img.shields.io/badge/Docker-Container-blue)
![Trivy](https://img.shields.io/badge/Security-Trivy-green)
![OWASP](https://img.shields.io/badge/Security-OWASP%20Dependency%20Check-orange)
![SonarQube](https://img.shields.io/badge/Code%20Quality-SonarQube-yellow)
![NodeJS](https://img.shields.io/badge/Runtime-Node.js-brightgreen)

---

# Project Overview

This project demonstrates a **complete DevSecOps CI/CD pipeline** that automates the process of building, analyzing, scanning, containerizing, and publishing an application.

Security is integrated throughout the pipeline to ensure vulnerabilities are detected **early in the software development lifecycle**.

The pipeline is implemented using **Jenkins** and integrates industry-standard DevSecOps tools including:

- SonarQube (Static Code Analysis)
- OWASP Dependency Check (Dependency Security)
- Trivy (Filesystem & Container Security)
- Docker (Containerization)

The goal of this project is to demonstrate **secure software delivery practices** by embedding security testing directly into the CI/CD workflow.

---

# DevSecOps Pipeline Architecture


---

# DevSecOps Workflow

The pipeline integrates **security testing at multiple stages**:

| Stage | Tool | Purpose |
|------|------|------|
| Code Quality | SonarQube | Detect bugs, vulnerabilities, code smells |
| Dependency Security | OWASP Dependency Check | Detect vulnerable third-party libraries |
| Filesystem Scan | Trivy | Scan project files for vulnerabilities |
| Containerization | Docker | Package application as container |
| Container Security | Trivy | Scan container image vulnerabilities |

This ensures vulnerabilities are caught **before the application reaches production**.

---

# Technologies Used

| Category | Tools |
|--------|------|
| CI/CD | Jenkins |
| Version Control | GitHub |
| Containerization | Docker |
| Static Code Analysis | SonarQube |
| Dependency Security | OWASP Dependency Check |
| Container Security | Trivy |
| Runtime | Node.js |
| Programming Language | JavaScript |

---

# Project Structure


| File | Description |
|-----|-------------|
| Jenkinsfile | Defines CI/CD pipeline stages |
| Dockerfile | Defines container build instructions |
| package.json | Node.js dependencies |
| app.js | Application source code |

---

# Jenkins Pipeline Stages

### 1. Clean Workspace
Removes previous build artifacts to ensure a clean environment.

### 2. Checkout Source Code
Pulls the latest code from GitHub.

### 3. SonarQube Analysis
Performs **static code analysis** to detect:

- bugs
- vulnerabilities
- code smells

### 4. Dependency Security Scan
OWASP Dependency Check scans for **vulnerable third-party libraries**.

### 5. Filesystem Scan
Trivy scans the project filesystem for:

- vulnerabilities
- exposed secrets
- misconfigurations

### 6. Install Dependencies
Installs required Node.js packages.

### 7. Docker Build
Builds a Docker container image for the application.

### 8. Docker Push
Pushes the built image to **Docker Hub registry**.

### 9. Container Image Scan
Trivy scans the Docker image for vulnerabilities.

---

# Prerequisites

Ensure the following tools are installed and configured:

- Jenkins
- Docker
- Git
- Node.js
- SonarQube Server
- OWASP Dependency Check
- Trivy

You will also need:

- Docker Hub account
- Jenkins credentials configuration
- SonarQube authentication token

---

# Setup Guide

## Clone the Repository

```bash
git clone https://github.com/39WA/devsecops-pipeline-project-1.git
cd devsecops-pipeline-project-1