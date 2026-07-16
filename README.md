# INTERN DETAILS 

   NAME : SURYA R M
   
   INTERN_ID : CITS4229
# Cloud Native CI/CD Pipeline

## Project Overview

This project demonstrates an end-to-end Continuous Integration and Continuous Deployment (CI/CD) pipeline using GitHub Actions and AWS EC2.

The application is automatically deployed whenever changes are pushed to the GitHub repository, eliminating manual deployment processes and showcasing modern DevOps practices.

---

## Features

- Automated deployment using GitHub Actions
- Secure deployment using SSH authentication
- Cloud hosting using AWS EC2
- Continuous Integration and Continuous Deployment workflow
- Zero manual intervention after code push
- Apache web server configuration on Amazon Linux

---

## Architecture

```text
Developer
    ↓
GitHub Repository
    ↓
GitHub Actions Workflow
    ↓
AWS EC2 Instance
    ↓
Automated Website Deployment
```

---

## Technologies Used

| Technology | Purpose |
|------------|----------|
| HTML | Frontend Development |
| CSS | Styling |
| Git | Version Control |
| GitHub | Source Code Management |
| GitHub Actions | CI/CD Automation |
| AWS EC2 | Cloud Infrastructure |
| Amazon Linux 2023 | Server Operating System |
| Apache HTTP Server | Web Hosting |
| SSH | Secure Remote Access |

---

## Project Structure

```text
Cloud-Native-CICD-Pipeline/
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── screenshots/
│
├── index.html
├── style.css
├── README.md
└── LICENSE
```

---

## Workflow

1. Developer pushes code changes to GitHub.
2. GitHub Actions workflow is triggered automatically.
3. Workflow authenticates with AWS EC2 using SSH keys.
4. Updated application files are copied to the server.
5. Apache serves the latest version of the website.

---

## AWS Configuration

### EC2 Configuration
- Instance Type: t3.micro
- Operating System: Amazon Linux 2023
- Region: ap-south-1 (Mumbai)

### Security Group Rules

| Type | Port |
|------|------|
| SSH | 22 |
| HTTP | 80 |

---

## GitHub Secrets

The following repository secrets were configured:

| Secret Name | Description |
|-------------|-------------|
| EC2_HOST | Public IP address of EC2 instance |
| EC2_USER | EC2 username |
| EC2_SSH_KEY | Private SSH key for authentication |

---

## Deployment Steps

### Launch EC2 Instance

Create an Amazon Linux EC2 instance and configure security groups.

### Install Apache Server

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Configure GitHub Secrets

Add the following secrets in:

```text
Repository → Settings → Secrets and Variables → Actions
```

- EC2_HOST
- EC2_USER
- EC2_SSH_KEY

### Configure GitHub Actions

Create a workflow file inside:

```text
.github/workflows/deploy.yml
```

The workflow automatically deploys the application whenever changes are pushed to the `main` branch.

---

## Screenshots

### EC2 Instance
![EC2 Instance](screenshots/ec2-instance.png)

### Security Group Configuration
![Security Group](screenshots/security-group.png)

### GitHub Secrets
![GitHub Secrets](screenshots/github-secrets.png)

### GitHub Actions Workflow
![GitHub Actions](screenshots/github-actions.png)

### Automated Deployment Dashboard
![Dashboard](screenshots/final-dashboard.png)

---

## Learning Outcomes

- Understanding CI/CD concepts
- Implementing deployment automation
- Working with GitHub Actions workflows
- Configuring AWS EC2 infrastructure
- Managing Linux servers
- Using GitHub Secrets securely
- Deploying applications in cloud environments

---

## Future Enhancements

- Docker containerization
- Infrastructure as Code using Terraform
- Monitoring with CloudWatch
- SSL configuration using HTTPS
- Multi-environment deployment pipeline

---


