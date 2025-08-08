# 🔁 Task 05 – Automate Strapi Deployment with GitHub Actions + Terraform

## ✅ Objective
Set up CI/CD pipelines using GitHub Actions and Terraform.

---

## 🔧 CI Workflow (`ci.yml`)

- Trigger: Push to `main`
- Actions:
  - Build Docker image
  - Push to Docker Hub
  - Save image tag as output

## 🔧 CD Workflow (`terraform.yml`)

- Trigger: Manual (`workflow_dispatch`)
- Actions:
  - Terraform `init`, `plan`, `apply`
  - Deploy updated image to EC2

---

## 🧩 Challenges Faced

- **Issue:** Terraform deployment failed.
- **Fix:** Regenerated IAM keys and updated GitHub Secrets

---

## 📦 Artifacts

- `.github/workflows/ci.yml`
- `.github/workflows/terraform.yml`
- Terraform files

---

## 🔗 Links

- [Loom Video](#)
- [Pull Request](#)