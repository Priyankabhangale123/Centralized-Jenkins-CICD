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
<img width="1920" height="984" alt="Priyankabhangale123_nodejs - Google Chrome 24-03-2026 22_35_13" src="https://github.com/user-attachments/assets/edba1ac9-c887-4316-8db2-57b4d792fca9" />

## Python Application
```
app-python/
├── app.py
├── Dockerfile
└── Jenkinsfile
```
<img width="1920" height="1020" alt="Priyankabhangale123_nodejs - Google Chrome 24-03-2026 22_37_01" src="https://github.com/user-attachments/assets/e7c6c08e-2b0a-427a-a39d-5a3fab9e048c" />

## Jenkins Setup (AWS EC2)
Jenkins is deployed on an EC2 instance and configured for centralized pipeline execution.

## Setup Steps
1. Launch EC2 instance
2. Install Java & Jenkins
3. Install required plugins
4. Configure Docker
5. Add Jenkins agent
6. Configure credentials
7. Connect shared library

<img width="1352" height="622" alt="Priyankabhangale123_nodejs - Google Chrome 24-03-2026 22_47_38" src="https://github.com/user-attachments/assets/c56c1d7a-df48-4ca7-959d-a0bf1d2088c2" />

## Build Agent Configuration
A dedicated Jenkins agent is used to execute builds:
```
Name: docker-agent
Executors: 1
Label: docker
Connection: SSH
```

![WhatsApp Image 2026-03-24 at 10 58 38 PM](https://github.com/user-attachments/assets/6c7f117d-180c-4a48-bf22-de72801cfc59)

## Shared Library Integration
Configured under:
```
Manage Jenkins → System → Global Pipeline Libraries
```
```
Library Name: shared-library-config
```

<img width="1364" height="636" alt="centralized-jenkins-cicd_README md at master · monikagaikwad22_centralized-jenkins-cicd - Google Chrome 24-03-2026 23_04_22" src="https://github.com/user-attachments/assets/150f188c-2d0c-4b06-92b7-9a172db09837" />

## Pipeline Setup
Separate pipelines are created for each application:
app-nodejs-pipeline
<img width="1920" height="1020" alt="app-python Config - Jenkins - Google Chrome 24-03-2026 23_51_11" src="https://github.com/user-attachments/assets/d1d2eff7-6779-4bcc-8be6-b65814aedf44" />

## Pipeline Workflow
Each pipeline executes standardized stages:

* Checkout source code
* Build application
* Run basic tests
* Perform security scan
* Deploy or build Docker image

<img width="1228" height="583" alt="Starting Jenkins - Google Chrome 25-03-2026 23_01_33" src="https://github.com/user-attachments/assets/0159a331-5cd8-4a54-98de-618e95a8eb43" />
<img width="1222" height="508" alt="centralized-jenkins-cicd_README md at master · monikagaikwad22_centralized-jenkins-cicd - Google Chrome 25-03-2026 23_03_42" src="https://github.com/user-attachments/assets/b97863f7-e2c5-44e3-be79-ede332ed15c4" />

## Deliverables
* Centralized Jenkins CI/CD system
* Shared pipeline library
* Multi-application pipeline setup
* Automated Docker image builds

## Learning Outcomes
* CI/CD automation using Jenkins
* Shared library implementation
* AWS-based infrastructure setup
* Multi-project pipeline management

## Conclusion
The centralized CI/CD platform ensures consistent and reusable pipelines across multiple applications. This approach significantly improves scalability and simplifies CI/CD management.









