# Discover Dollar – Full Stack CRUD Application (MEAN Stack)

## 📌 Project Overview

This project is a full-stack CRUD application built using the MEAN stack (MongoDB, Express.js, Angular, Node.js). It allows users to create, read, update, and delete tutorials.

The application is fully containerized using Docker and orchestrated with Docker Compose to ensure consistent deployment and environment configuration.

---

## 🏗 Architecture

Frontend (Angular)  
→ communicates with → Backend (Node.js + Express)  
→ connects to → MongoDB  

All services run as isolated containers inside a Docker network.

---

## 🛠 Tech Stack

- Frontend: Angular 15
- Backend: Node.js, Express.js
- Database: MongoDB
- ORM: Mongoose
- Containerization: Docker
- Orchestration: Docker Compose
- Web Server: Nginx

---

## 📁 Project Structure

crud-dd-task-mean-app/
│
├── backend/
│ ├── app/
│ ├── Dockerfile
│ └── server.js
│
├── frontend/
│ ├── src/
│ ├── Dockerfile
│ └── nginx.conf
│
├── docker-compose.yml
└── README.md

---

## ⚙️ Environment Configuration

The backend uses environment variables for database configuration:

MONGO_URL=mongodb://mongodb:27017/dd_db

This makes the application flexible for:

- Local development  
- Docker environments  
- Cloud deployments  

---

## 🚀 How to Run the Project

### Option 1: Run Using Docker (Recommended)

From the project root directory:

docker compose up --build

Access the application:

Frontend:  
http://localhost:8081  

Backend API:  
http://localhost:8080/api/tutorials  

To stop:
docker compose down

---

### Option 2: Run Without Docker

1. Start MongoDB locally  

2. Navigate to backend folder:

npm install
node server.js

3. Navigate to frontend folder:

npm install
ng serve


---

## ✅ Features

- Add tutorial  
- View tutorials  
- Update tutorial  
- Delete tutorial  
- Persistent MongoDB storage using Docker volumes  
- Health checks for backend container  
- Clean project structure  
- Environment-based configuration  

---

## 🐳 Docker Setup

Services defined in docker-compose:

- mongodb  
- backend  
- frontend  

MongoDB data is persisted using a named Docker volume:

mongo-data

---

## 📦 Improvements Applied

- Removed hardcoded database URL  
- Added environment variable support  
- Added Docker healthcheck  
- Cleaned `.gitignore`  
- Removed obsolete compose version field  
- Production build for Angular frontend  

---

## 📬 Author

Abhishek Gunagi  
GitHub: https://github.com/AbhishekGunagi
LinkedIn: https://www.linkedin.com/in/abhishek-gunagi-395741249/
