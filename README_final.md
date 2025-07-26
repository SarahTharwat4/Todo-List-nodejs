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



✅ Todo App - DevOps Track (Part 2 Completed)
🧰 Tasks:
✅ Created a Linux VM

✅ Installed Docker using Ansible

✅ Pulled the Docker image inside the VM

✅ Handled architecture mismatch by rebuilding the image from source

✅ Fixed environment variable issues

✅ Ran the container successfully on port 4000

⚙️ Run Details:
Container started successfully on the VM at:

http://192.168.42.106:4000

To test it :
curl http://192.168.42.106:4000
📂 Notes:
Used Ansible playbook to automate Docker installation

Rebuilt the image manually inside the VM to match system architecture

Created and used .env file to inject environment variables

Exposed correct port (4000) and verified the app is running via browser and curl








