# 🔵🟢 Task 11 – Blue/Green Deployment with CodeDeploy

## ✅ Objective
Enable zero-downtime deployment using CodeDeploy and ALB routing.

---

## 🔧 Setup Overview

- ECS Cluster with Fargate
- ALB with two Target Groups (Blue & Green)
- CodeDeploy Application and Deployment Group
- Canary strategy: 10% for 5 minutes

---

## 🧩 Challenges Faced

- **Issue:** ECS service failed and Traffic not switching
- **Fix:** Port mapins and taskdefination setted correctly Corrected ALB listener rules and target group weights

---

## 📦 Artifacts

- Terraform setup for CodeDeploy
- Deployment logs

---

## 🔗 Links

- [Loom Video/Screenshots](#)
- [Pull Request](#)