# Assignment 2: GitHub Actions Workflow for Docker Image 

This repository contains a **GitHub Actions workflow** that automates building and pushing Docker images to Docker Hub for different environments: **development, staging, and production**.

---

## Features  
✅ Automates Docker image builds for **dev, staging, and production** environments.  
✅ Tags Docker images appropriately (`dev`, `staging`, `latest`).  
✅ Pushes images to **Docker Hub** securely.  
✅ Triggers workflow **only on relevant branch updates**.  
✅ Uses **GitHub Secrets** for security.  

## Set Up GitHub Secrets
Before running the workflow, add the following secrets in GitHub → Settings → Secrets and variables → Actions:

### Secret Name	Description
**`DOCKERHUB_USERNAME`	Your Docker Hub username**
**`DOCKERHUB_TOKEN`	Your Docker Hub access token**

Go to Docker Hub.
Navigate to Account Settings → Security.
Create a New Access Token and copy it.
Store it in GitHub Secrets as DOCKERHUB_TOKEN.

1) Push Code to Relevant Branch
Commit and push your changes to trigger the workflow:

`git add .`
`git commit -m "Implemented GitHub Actions workflow"`
`git push origin dev  # or staging/main`

2) Monitor Workflow Execution
Go to GitHub → Your Repository → Actions to check the workflow status.

3) Verify Docker Image on Docker Hub
Log in to Docker Hub and confirm the image was successfully pushed.
