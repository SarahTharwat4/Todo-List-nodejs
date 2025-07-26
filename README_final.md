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
# ✅ Todo App - DevOps Track (Part 2 Completed)

## 🔧 Project Summary:

This part focuses on using Ansible to remotely install Docker on a Linux VM.

- Created a local Ubuntu VM (via VirtualBox)
- Configured SSH access to the VM
- Used Ansible from host machine to:
  - Install Docker
  - Enable and start Docker service
  - Verify installation

---

## 📝 Tasks Completed:

- ✅ Created Ubuntu VM with SSH access
- ✅ Created Ansible inventory file
- ✅ Wrote `docker-setup.yml` playbook
- ✅ Installed Docker remotely using Ansible
- ✅ Verified Docker installation

---

## 📂 Files Included:

- `docker-setup.yml`: Playbook to install and start Docker
- `inventory.ini.example`: Sample inventory with SSH config

---

## 🚀 How to Run:

```bash
cp inventory.ini.example inventory.ini
ansible-playbook -i inventory.ini docker-setup.yml
ansible -i inventory.ini my_vm -a "docker --version"


📋 Result:
192.168.42.106 | SUCCESS | rc=0 >>
Docker version 24.0.5, build ced0996










