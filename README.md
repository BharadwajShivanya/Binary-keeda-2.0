# Binary-keeda-2.0

This repository contains a **Dockerized React application** with clean **development and production setups**, proper **environment variable handling**, and a **GitHub-ready structure**.

---

## 🚀 Tech Stack

- React (Create React App)
- Docker & Docker Compose
- Node.js
- Nginx (Production)
- Environment Variables
- GitHub

---

## 📁 Project Structure

react-compose/
├── Dockerfile
├── docker-compose.dev.yml
├── docker-compose.prod.yml
├── .env.example
├── .gitignore
├── package.json
├── package-lock.json
├── public/
└── src/

---

## 🔐 Environment Variables

This project uses environment variables for configuration.

### 📄 `.env.example`

A sample file is already provided.

Create your local `.env` file using:

```bash
cp .env.example .env
⚠️ Important
Never commit .env
.env is already ignored via .gitignore
🧪 Development Mode (Hot Reload)
Runs the React app inside Docker using npm start.
▶ Command
docker compose -f docker-compose.dev.yml up --build
🌐 Open in Browser
http://localhost:3000
🧠 What happens
Uses Node container
Code mounted as volume
Hot reload enabled
Best for development
🚀 Production Mode (Optimized Build)
Builds the React app and serves it via Nginx.
▶ Command
docker compose -f docker-compose.prod.yml up --build
🌐 Open in Browser
http://localhost:8080
🧠 What happens
Multi-stage Docker build
npm run build
Static files served via Nginx
Optimized production setup
🛑 Stop Containers
docker compose down
🧹 Optional: Clean Docker System
docker system prune -a
📄 Dockerfile Overview
Stage 1: Install dependencies & build React app
Stage 2: Serve build output using Nginx
Smaller image size
Faster startup
Production best practices followed
📦 Git & GitHub Setup
Initialize Repository
git init
git branch -M main
git remote add origin https://github.com/BharadwajShivanya/Binary-keeda-2.0.git
Commit & Push Code
git add .
git commit -m "dockerized react app with dev and prod setup"
git push origin main
❌ Ignored Files (.gitignore)
node_modules
.env files
build output
logs
OS specific files
Keeps repository clean and secure.
✅ Current Status
✔ Docker Dev working (port 3000)
✔ Docker Prod working (port 8080)
✔ Environment variables handled correctly
✔ GitHub repository synced
✔ Production-ready setup
