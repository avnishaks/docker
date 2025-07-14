## 🐳 Docker Handbook – Quick Start Guide

This guide explains how to build, run, manage, and push Docker images — using the repo:  
🔗 **[avnishaks/batman_image on Docker Hub](https://hub.docker.com/repository/docker/avnishaks/batman_image)**

---

### 🛠️ Build Docker Image

```bash
# 📦 Build the image from Dockerfile
docker build -t batman_image .


# 🏷️ Tag the image with your Docker Hub repo
docker tag batman_image avnishaks/batman_image:latest

🔐 Login to Docker Hub
docker login

🚀 Push to Docker Hub
docker push avnishaks/batman_image:latest

▶️ Run a Container from the Image
docker run -it avnishaks/batman_image

🌐 Port Mapping

If your app runs on a specific port (e.g., 3000), expose it like this:
docker run -it -e PORT=3000 -p 3000:3000 batman_image
Option	Description
-p 3000:3000	Maps port 3000 on the host to port 3000 in the container
-e PORT=3000	Passes the environment variable PORT=3000 to the container 
🌍 Now access your app via http://localhost:3000



📄 List Docker Images
docker images

📋 List Running Containers
docker ps

🛑 Stop a Running Container
docker stop <container_id>


❌ Remove a Container
docker rm <container_id>

🧹 Remove an Image
docker rmi <image_id>
# Or force remove
docker rmi -f <image_id>


🧼 Clean All Unused Resources (Optional)
docker system prune -a


🚀 Common Docker Compose Commands

🆙 Start all services
docker-compose up

➡️ Add -d to run in detached mode (background):
docker-compose up -d

🛑 Stop services
docker-compose down
➡️ To remove volumes as well:
docker-compose down -v

🔄 Restart services
docker-compose restart

🔁 Rebuild images (if Dockerfile changed)
docker-compose up --build






🔗 References
🐋 Dockerfile Docs: https://docs.docker.com/engine/reference/builder/
🧰 Docker CLI Reference: https://docs.docker.com/engine/reference/commandline/docker/



---

Let me know if you want this tailored for a specific app or CI/CD pipeline too!
