# 🧪 Task 07 – ECS Deployment via GitHub Actions

## ✅ Objective
Automate ECS deployment using GitHub Actions only.

---

## 🔧 Workflow Highlights

- Build and tag Docker image
- Push to ECR
- Update ECS Task Definition
- Deploy new revision

---

## 🧩 Challenges Faced

- **Issue:**  ECS deployment failed and Task revision not updated
- **Fix:** Inspected container logs to startup  issues
          Used AWS CLI to register new task definition with updated image

---

## 📦 Artifacts

- `.github/workflows/deploy.yml`
- Terraform ECS setup

---

## 🔗 Links

- [Loom Video/Screenshots](#)
- [Pull Request](#)