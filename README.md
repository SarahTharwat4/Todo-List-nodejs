
🛠️ DevOps Internship Assessment - Todo List App
📌 Overview
This project demonstrates my understanding of core DevOps practices using a simple Todo List web application.
The app was dockerized, deployed on a VM using Ansible and Docker Compose, and configured to auto-update using Watchtower.

💡 I used ChatGPT as a learning assistant to help guide me through the process, but all implementations were done by me.

📚 Table of Contents
Part 1: Docker & GitHub Actions CI

Part 2: Ansible VM Setup

Part 3: Docker Compose & Auto Updates

✅ Part 1: Docker & GitHub Actions CI
Forked the original repo: Ankit6098/Todo-List-nodejs

Added a Dockerfile to containerize the application.

Created a private DockerHub repo.

Configured GitHub Actions to:

Build the Docker image on push.

Push the image to DockerHub automatically.

📂 Main File:

bash
Copy
Edit
.github/workflows/docker-image.yml
⚙️ Part 2: Ansible VM Setup
Created an Ubuntu VM using VirtualBox.

Connected via SSH from my local machine.

Used Ansible from local to:

Install Docker & Docker Compose.

Prepare the machine for deployment.

📂 Files:

inventory.ini – Contains VM IP.

playbook.yml – Ansible playbook for provisioning.

🔄 Part 3: Docker Compose & Auto Updates
Deployed the app and Watchtower using docker-compose.yml.

Added healthcheck to the app container.

Watchtower monitors DockerHub for new image versions and auto-pulls updates every 30 seconds.

📂 Snippet from docker-compose.yml:

yaml
Copy
Edit
watchtower:
  image: containrrr/watchtower
  volumes:
    - /var/run/docker.sock:/var/run/docker.sock
  command: --interval 30
✅ I tested auto-update by pushing a new image version to DockerHub. Watchtower detected it and redeployed the updated container successfully.

🧰 Tools & Technologies
Docker & Docker Compose

GitHub Actions

DockerHub

Ansible

Watchtower

VirtualBox (Local VM)
