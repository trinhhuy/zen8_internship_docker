# Zen8labs internship

## 🚀 Getting Started

This guide will help you set up and run the project using **Docker Compose**.

### **1. Clone the Repository**
Make sure you have **Git** installed, then run:
```bash
git clone --recurse-submodules <repository-url>
```
If you forgot to clone with submodules, you can run:
```bash
git submodule update --init --recursive
```

### **2. Set Up Environment Variables**
Create a `.env` file in the project root:
```bash
cp .env.example .env
```
Edit the `.env` file and update necessary variables:
```bash
nano .env
```

### **3. Build and Run the Containers**
Ensure **Docker** and **Docker Compose** are installed, then run:
```bash
docker-compose up -d --build
```
This will build and start all services in detached mode.

### **4. Check Running Containers**
To verify that all containers are running:
```bash
docker ps
```

### **5. Access the Application**
Once the services are running, access the application via:
```
http://localhost:PORT
```
(Replace `PORT` with the port defined in `.env` or `docker-compose.yml`.)

### **6. Stopping and Restarting**
To stop the running containers:
```bash
docker-compose down
```
To restart the project:
```bash
docker-compose up -d
```

### **7. Updating the Repository and Submodules**
If the repository or submodules have been updated, run:
```bash
git pull --recurse-submodules
```
Then rebuild the containers:
```bash
docker-compose up -d --build
```

### **8. Troubleshooting**
- Check logs for errors:
  ```bash
  docker-compose logs -f
  ```
- Restart a specific service:
  ```bash
  docker-compose restart <service_name>
  ```
- Remove all containers and volumes (⚠️ Data loss warning):
  ```bash
  docker-compose down -v
  ```

### **9. Additional Commands**
- Enter a running container:
  ```bash
  docker exec -it <container_name> sh
  ```
- List all Docker volumes:
  ```bash
  docker volume ls
  ```
- Prune unused Docker objects:
  ```bash
  docker system prune -a --volumes -f
  ```

### 📜 **License**
This project is licensed under the **Zen8labs License**.

---

If you have any issues, feel free to create an issue or reach out! 🚀

