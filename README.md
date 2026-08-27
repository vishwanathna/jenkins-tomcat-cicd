# jenkins-tomcat-cicd

# 🚀 CI/CD Pipeline Automation Using Jenkins & Apache Tomcat

![Java](https://img.shields.io/badge/Java-17-orange?logo=openjdk)
![Maven](https://img.shields.io/badge/Maven-Build-C71A36?logo=apachemaven)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-D24939?logo=jenkins)
![Tomcat](https://img.shields.io/badge/Apache%20Tomcat-9-F8DC75?logo=apachetomcat)
![GitHub](https://img.shields.io/badge/GitHub-Source%20Control-181717?logo=github)
![AWS](https://img.shields.io/badge/AWS-Cloud-FF9900?logo=amazonaws)

> Automated CI/CD pipeline for building and deploying a Java web application using Jenkins, Maven, GitHub, and Apache Tomcat on AWS.

---

## 📌 Project Overview

This project demonstrates the implementation of a Jenkins-based CI/CD pipeline for a Java web application called **MovieHub**.

The pipeline automates the application delivery process from source code checkout to deployment on Apache Tomcat.

### CI/CD Workflow

```text
Developer
    │
    │ Git Push
    ▼
 GitHub
    │
    │ Webhook
    ▼
 Jenkins
    │
    ├── Git Checkout
    │
    ├── Maven Build
    │
    └── WAR Artifact
            │
            ▼
      Tomcat Deployment
            │
            ▼
     MovieHub Application
```

##### 🏗️ Architecture

The application is deployed using separate AWS EC2 environments for Jenkins and Apache Tomcat.
```text
                         ┌─────────────────┐
                         │     GitHub      │
                         │  Source Code    │
                         └────────┬────────┘
                                  │
                              Webhook
                                  │
                                  ▼
                         ┌─────────────────┐
                         │     Jenkins     │
                         │    AWS EC2      │
                         └────────┬────────┘
                                  │
                    ┌─────────────┼─────────────┐
                    │             │             │
                    ▼             ▼             ▼
              Git Checkout   Maven Build    WAR File
                                                │
                                                ▼
                                      ┌─────────────────┐
                                      │ Apache Tomcat   │
                                      │     AWS EC2     │
                                      └────────┬────────┘
                                               │
                                               ▼
                                      MovieHub Application
```
🛠️ Technologies Used

| Technology          | Purpose                       |
| ------------------- | ----------------------------- |
| AWS EC2             | Cloud infrastructure          |
| GitHub              | Source code management        |
| Jenkins             | CI/CD automation              |
| Java 17             | Application platform          |
| Maven               | Build and packaging           |
| Apache Tomcat 9     | Application server            |
| GitHub Webhooks     | Automatic pipeline triggering |
| Deploy to Container | Automated Tomcat deployment   |
| Linux               | Server administration         |

💡 Project Outcome:

This project demonstrates how a manual Java application deployment process can be converted into an automated CI/CD workflow.

Instead of manually building and deploying the application, a developer can push code to GitHub and allow Jenkins to automatically perform:

Checkout → Build → Package → Deploy

This provides a repeatable and consistent application delivery process.

<img width="1241" height="605" alt="01-jenkins-pipeline png" src="https://github.com/user-attachments/assets/a3391fe9-f473-4a2d-880d-3861805c4667" />
