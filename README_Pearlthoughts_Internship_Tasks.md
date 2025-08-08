# Internship Task Summary @ Pearlthoughts

**Intern Name:** Harika Baddam  
**Internship Domain:** DevOps, AWS, Docker, CI/CD  
**Focus Areas:** Strapi Deployment, Terraform, Docker, GitHub Actions, ECS Fargate, Blue/Green Deployments, Monitoring

---

## ✅ Completed Tasks Overview

### **Task 1:** Strapi Local Setup
- Cloned official Strapi repo and ran it locally.
- Explored folder structure and created sample content types.
- ✅ GitHub repo updated with setup steps and Loom video.

### **Task 2:** Dockerize Strapi
- Created `Dockerfile` for the Strapi app.
- Verified local build and container run.

### **Task 3:** Docker Compose Environment
- Created Docker network with:
  - Strapi container
  - PostgreSQL container
  - Nginx reverse proxy (port 80)
- Ensured all containers work on the same Docker network.
- Accessed Strapi at `http://localhost`.

### **Task 4:** Deploy Strapi on EC2 with Terraform + Docker
- Built and pushed Docker image to Docker Hub/ECR.
- Wrote Terraform script to:
  - Launch EC2
  - Install Docker via user data
  - Pull and run Strapi image

### **Task 5:** Automate Strapi Deployment with GitHub Actions + Terraform
- CI workflow:
  - On push → Build Docker image → Push to ECR
- CD workflow:
  - Manual trigger → Terraform apply → Deploy on EC2

### **Task 6:** Deploy Strapi on AWS ECS Fargate (via Terraform)
- Dockerized app pushed to ECR
- Wrote Terraform code for:
  - VPC, subnets, IGW
  - ECS cluster, task, service (Fargate)
  - ALB + Security Groups
- Public URL exposes Strapi app.

### **Task 7:** ECS Fargate + GitHub Actions CI/CD (Fully Automated)
- Created GitHub workflow to:
  - Build, tag, and push Docker image
  - Update ECS Task Definition with new image
  - Trigger ECS deployment via Terraform

### **Task 8:** Add CloudWatch Monitoring
- Created CloudWatch log group using Terraform
- Integrated AWS Logs driver in ECS Task Definition
- Enabled metrics for:
  - CPU, Memory, Network, Task Count
- Configured dashboards and alarms (optional)

### **Task 9:** Use AWS Fargate Spot Instances
- Updated Fargate service to use `FARGATE_SPOT` to save costs

### **Task 10:** Strapi Admin Configuration
- Logged into deployed Strapi
- Created Content Types and API endpoints
- Configured roles and permissions
- Verified public API access via ALB URL

### **Task 11:** Blue/Green Deployment on ECS
- Created:
  - ECS Cluster & Service (Fargate)
  - ALB with Blue & Green target groups
  - ECS Task Definition (dynamic image)
  - CodeDeploy App + Deployment Group (Canary/AllAtOnce)
- Setup rollback, health checks, and dynamic switching

### **Task 12:** GitHub Actions to Automate Blue/Green Deployment
- GitHub workflow handles:
  - Docker image push with commit SHA tag
  - ECS Task Definition update with new tag
  - Trigger CodeDeploy deployment
  - Optional: monitor and rollback

### **Task 13:** Docker Swarm CronJob Research
- Created a detailed research document with:
  - Cronjob concepts in Docker Swarm
  - Workarounds using cron + service
  - Example setups
  - Added screenshots and pushed to GitHub

### **Task 14:** Unleash Documentation
- Explained what Unleash is
- How to integrate with a local React app
- Setup steps and usage included

---

## 🧩 Common Issues Faced

- **Docker Image Tag Conflicts:** Solved by using GitHub commit SHA for tagging.
- **Terraform State Conflicts:** Resolved by using backend S3 or local locking.
- **Port conflicts on localhost:** Solved using custom Docker networks.
- **Strapi build failures on EC2:** Fixed with correct Node version and persistent volumes.
- **Permission errors in ECS:** Fixed IAM roles for ECS task execution and ECR pull.
- **Blue/Green mismatch:** Solved by correctly mapping target groups and listener rules.
- **CloudWatch not showing logs:** Fixed by ensuring log group and task definition config match.

---

## 🧰 Tools & Tech Used

- **Languages:** YAML, HCL, Bash  
- **DevOps:** Docker, Docker Compose, GitHub Actions  
- **Cloud:** AWS (ECS, EC2, ECR, ALB, CloudWatch, IAM)  
- **IaC:** Terraform  
- **Backend:** Strapi  
- **Monitoring:** AWS CloudWatch  
- **Version Control:** Git, GitHub

---

## 📎 Final Note

Each task has been pushed to a separate branch or folder in the GitHub repository with:
- Source code
- Terraform scripts
- GitHub Actions workflows
- Screenshots or Loom video
- Proper documentation (`README.md`)
