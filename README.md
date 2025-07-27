
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


Part 4 - Bonus: Kubernetes and ArgoCD (Overview)
For the bonus part, the task requires deploying the application using Kubernetes instead of Docker Compose on the VM, and managing continuous deployment using ArgoCD.

What is Kubernetes?
Kubernetes is a powerful container orchestration tool that automates deployment, scaling, and management of containerized applications.

What is ArgoCD?
ArgoCD is a declarative, GitOps continuous delivery tool for Kubernetes. It syncs your Kubernetes manifests from a Git repository and ensures the cluster state matches the desired state.

My approach (Summary):
Due to time constraints and complexity, I provided an overview and a plan for Part 4 rather than a full implementation.

I understand that:

Kubernetes will replace Docker Compose for managing the app deployment.

ArgoCD will be used to automate deployment updates via syncing from the Git repository.

To fully implement, one would:

Create Kubernetes manifests (Deployment, Service, ConfigMap, etc.).

Install and configure ArgoCD on the VM.

Connect ArgoCD to the Git repo containing manifests.

Use ArgoCD UI or CLI to manage application lifecycle and updates.

Why is this important?
Kubernetes and ArgoCD represent industry standards for modern, scalable, and automated deployments.

Implementing these tools shows advanced DevOps capabilities.
