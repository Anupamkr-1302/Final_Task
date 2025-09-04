# CI/CD Pipeline with GitHub Actions & Docker

This project demonstrates a simple **CI/CD pipeline** using GitHub Actions and Docker Hub.  
The pipeline builds and tests a small Node.js application, packages it into a Docker image,  
and pushes the image to Docker Hub. The image can then be deployed locally using Docker Compose.

---

## 🎯 Objective
- Automate build and test steps with GitHub Actions  
- Package the app into a Docker image  
- Push the image to Docker Hub  
- Deploy the container locally  

---

## 🛠 Tools Used
- GitHub Actions (CI/CD automation)  
- Docker & Docker Hub (containerization and registry)  
- Docker Compose (local deployment)  
- Node.js (basic app and test setup)  

---

## ⚙️ Pipeline Workflow
The GitHub Actions workflow runs on each push to `main`:
1. Checkout the repository  
2. Set up Node.js  
3. Install dependencies and run test script  
4. Log in to Docker Hub  
5. Build or prepare a container image  
6. Push the image to Docker Hub  

---

## 📂 Project Files
- `.github/workflows/deploy.yml` → CI/CD pipeline definition  
- `app.js` → minimal Node.js web server  
- `Dockerfile` → defines how the image is built  
- `docker-compose.yml` → deploys the app locally on port 3000  
- `package.json` → Node.js metadata and scripts  
- `README.md` → project documentation  

---

## ▶️ Run Locally
After the workflow pushes your image to Docker Hub:

```bash
docker compose up
