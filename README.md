# Centralized-Jenkins-CICD
# 🚀 Centralized CI/CD Platform with Shared Jenkins Library
## 📌 Overview
This project demonstrates the implementation of a centralized CI/CD system using Jenkins, designed to support multiple applications through a shared pipeline library.

Instead of managing separate Jenkins setups for each application, a single Jenkins instance is used to enforce standardized CI/CD workflows, improving efficiency and maintainability.

<img width="1536" height="1024" alt="ChatGPT Image Mar 12, 2026, 11_10_04 PM" src="https://github.com/user-attachments/assets/f1890b64-e354-4cdc-bd44-56c47e9e79eb" />

## Objectives
* Build a centralized CI/CD infrastructure
* Standardize pipeline stages across applications
* Reduce duplication and manual effort
* Improve security and consistency

## Tech Stack
* Jenkins
* GitHub
* AWS EC2
* Jenkins Shared Library

## Architecture Summary

The system follows a centralized pipeline execution model:
```
Developers
   ↓
GitHub Repositories
   ↓
Jenkins Server (AWS EC2)
   ↓
Shared Pipeline Library
   ↓
Jenkins Agent (Docker-based)
   ↓
Build → Test → Scan → Deploy
  ```
## Repository Structure

## Shared Library
```
jenkins-shared-library/
└── vars/
    └── cicdPipeline.groovy
```

 ## NodeJS Application
```
app-nodejs/
├── app.js
├── package.json
├── Dockerfile
└── Jenkinsfile
```
