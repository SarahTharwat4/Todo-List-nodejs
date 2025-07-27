
Todo List NodeJS - DevOps Internship Assessment
Overview
This repository contains the implementation for the DevOps Internship Assessment task. The task is divided into 4 parts, covering cloning, dockerizing, setting up CI/CD, provisioning VM, and using orchestration tools.

Part 1: Dockerize & CI Pipeline (30 points)
Clone the original repo: https://github.com/Ankit6098/Todo-List-nodejs

Use your own MongoDB database connection (configured via .env).

Dockerize the Node.js application by creating a Dockerfile.

Create a GitHub Actions CI pipeline to build the Docker image and push it to a private Docker registry (Docker Hub in this case).

What I did:
Forked the original repo.

Created a Dockerfile to containerize the app.

Created .github/workflows/ci.yml to automate the build and push process on each push to main branch.

Used my Docker Hub account for image hosting.

Part 2: VM Provisioning & Ansible (30 points)
Created a Linux VM locally (using VirtualBox).

Used Ansible from my local machine to provision the VM and install required packages, including Docker and Docker Compose.

Configured Ansible playbook to automate VM setup.

What I did:
Set up Ubuntu VM and configured SSH access.

Created Ansible playbook to:

Install Docker

Install Docker Compose

Set up required system dependencies.

Part 3: Docker Compose & Auto-update (40 points)
Used Docker Compose on the VM to run the app container.

Configured health checks in the docker-compose.yml for container status monitoring.

Installed and configured Watchtower to automatically monitor Docker Hub for new images and update the container accordingly.

What I did:
Created docker-compose.yml file with the todo app and watchtower service.

Watchtower periodically checks Docker Hub for updated images and updates the running container.

Verified the container auto-updates by pushing new images and observing Watchtower logs.

Part 4: Kubernetes & ArgoCD (Bonus - 50 points)
Instead of Docker Compose, deployed the app using Kubernetes on the VM.

Used ArgoCD for Continuous Deployment to monitor the Kubernetes manifests and sync updates automatically.

What I did:
Installed Kubernetes cluster (using minikube or k3s) on the VM.

Created Kubernetes manifests (deployment, service) for the app.

Installed and configured ArgoCD to watch the GitHub repo and deploy changes automatically.

How to Run
Clone your forked repo.

Configure .env with your MongoDB URI.

Build and push Docker image using GitHub Actions.

Provision VM using Ansible.

Run docker-compose up -d to launch the app and watchtower.

For Kubernetes, deploy manifests and configure ArgoCD accordingly.

Notes
All sensitive info is stored in .env and never committed.

Used containrrr/watchtower for auto-updating containers due to simplicity and popularity.

Chose VirtualBox and Ubuntu for VM for compatibility and ease of use.

Kubernetes setup done with lightweight k3s for minimal resource consumption.
