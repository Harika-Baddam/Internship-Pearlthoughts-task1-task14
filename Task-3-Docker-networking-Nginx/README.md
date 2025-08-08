

```markdown
# 🌐 Task 03 – Docker Networking + Nginx Reverse Proxy

## ✅ Objective
Connect Strapi and PostgreSQL containers via Docker network and expose Strapi via Nginx on port 80.

---

## 🧱 Setup Overview

### Docker Compose

```yaml
version: '3'
services:
  strapi:
    build: .
    ports:
      - "1337:1337"
    networks:
      - strapi-net
    depends_on:
      - db

  db:
    image: postgres
    environment:
      POSTGRES_USER: strapi
      POSTGRES_PASSWORD: strapi
      POSTGRES_DB: strapi
    networks:
      - strapi-net

  nginx:
    image: nginx
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf
    ports:
      - "80:80"
    networks:
      - strapi-net

networks:
  strapi-net:
    driver: bridge

🧩 Challenges Faced
- Issue: Nginx returned 502 Bad Gateway.
- Fix: Ensured Strapi container was healthy and added proper proxy_set_header.
