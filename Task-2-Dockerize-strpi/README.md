
---

## 📁 Task-02-Dockerfile/README.md

```markdown
# 🐳 Task 02 – Dockerfile for Strapi

## ✅ Objective
Containerize the Strapi application using Docker.

---

## 📦 Dockerfile

```Dockerfile
FROM node:18-alpine

WORKDIR /app

COPY . .

RUN yarn install

EXPOSE 1337

CMD ["yarn", "develop"]
### Build and Run
docker build -t strapi-app .
docker run -p 1337:1337 strapi-app

🧩 Challenges Faced
- Issue: Container exited due to missing node_modules.
- Fix: Ensured COPY . . includes package.json and yarn.lock.

🔗 Links
- Loom Video
- Pull Request

