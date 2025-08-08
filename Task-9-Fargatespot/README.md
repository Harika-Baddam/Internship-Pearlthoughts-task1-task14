# 💸 Task 09 – Use AWS Fargate Spot

## ✅ Objective
Optimize ECS costs using Fargate Spot instances.

---

## 🔧 Steps Performed

- Updated ECS Service to use `FARGATE_SPOT` capacity provider
- Added fallback to regular Fargate

---

## 🧩 Challenges Faced

- **Issue:** Task placement failed and task stops every 5 minutes
- **Fix:** Defined capacity provider strategy with weights . Checked Cloudwatchlogs for fatal errors and confirmed DATABASE access(POSTGRESQL must be reachable) . Verified DB crentials and host

---

## 📦 Artifacts

- Terraform ECS service update

---

## 🔗 Links

- [Loom Video/Screenshots](#)
- [Pull Request](#)