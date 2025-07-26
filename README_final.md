# ✅ Todo App - DevOps Track (Part 1 Completed)

## 🔧 Project Summary:

This is a Node.js Todo List App that was:
- Dockerized using a custom `Dockerfile`
- Connected to MongoDB Atlas using `.env`
- Pushed to Docker Hub
- Built and tested locally

---

## 📝 Tasks Completed:

- ✅ Setup project & dependencies
- ✅ Connected to MongoDB Atlas via environment variables
- ✅ Created `Dockerfile`
- ✅ Built Docker image locally
- ✅ Logged in to Docker Hub from terminal
- ✅ Pushed Docker image manually to Docker Hub
- ✅ Tested image with `docker run`

---

## 📤 Docker Hub Image:

👉 [Click here to view image on Docker Hub](https://hub.docker.com/repository/docker/loop0x800/todo-app)

You can pull and run the image like this:

```bash
docker pull loop0x800/todo-app
docker run -p 3000:3000 loop0x800/todo-app

__________________________________________________________________________________________________

# Part 2 – Ansible

## 🔧 Files

- `docker-setup.yml`: Ansible playbook to install Docker on remote Ubuntu VM.
- `inventory.ini.example`: Sample inventory file with VM IP and SSH config.

## ✅ Requirements

- Ubuntu VM with SSH access (tested on 24.04).
- Ansible installed on the local machine.

## 🚀 How to Use

```bash
cp inventory.ini.example inventory.ini
ansible-playbook -i inventory.ini docker-setup.yml
ansible -i inventory.ini my_vm -a "docker --version"












