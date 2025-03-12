# 🚀 Start2Launch - Backend

Welcome to the **Start2Launch Backend** repository! This is the backend system for **Start2Launch**, a full-stack web application designed to help students and developers build, collaborate, and deploy projects seamlessly.  

The backend is built using **Spring Boot**, providing a secure and scalable REST API for authentication, project management, and real-time collaboration.  

---

## 📌 Features

✅ **User Authentication & Authorization** (OAuth 2.0, JWT)  
✅ **Project Management API** (CRUD operations for projects, tasks, and team members)  
✅ **Real-Time Collaboration** (Live chat, file sharing, code editing via WebSockets)  
✅ **Role-Based Access Control** (Admin, Team Lead, Developer, Viewer)  
✅ **Database Optimization** (Hybrid MySQL & MongoDB for structured & unstructured data)  
✅ **Scalable Deployment** (CI/CD with GitHub Actions, Docker, and Kubernetes)  

---

## 🏠 Tech Stack  

- **Backend:** Spring Boot, Java  
- **Security:** OAuth 2.0, JWT, Spring Security  
- **Database:** MySQL (Structured Data), MongoDB (Unstructured Data)  
- **Real-Time Communication:** WebSockets  
- **API Documentation:** Swagger  
- **DevOps:** Docker, Kubernetes, Jenkins, GitHub Actions  

---

## 📂 Project Structure

```
📛 start2launch-backend
 ├ 📚 src
 ├ ├ 📚 main
 ├ ├ ├ 📚 java/com/start2launch
 ├ ├ ├ ├ 📚 controller  # API Controllers
 ├ ├ ├ ├ 📚 service     # Business Logic
 ├ ├ ├ ├ 📚 repository  # Database Repositories
 ├ ├ ├ ├ 📚 config      # Security & App Configurations
 ├ ├ ├ ├ 📄 Start2LaunchApplication.java
 ├ ├ 📚 resources
 ├ ├ ├ 📄 application.yml  # Environment Config
 ├ ├ ├ 📄 schema.sql       # Database Schema
 ├ ├ ├ 📄 data.sql         # Sample Data
 ├ 📄 pom.xml  # Maven Dependencies
 ├ 📄 README.md  # Project Documentation
```

---

## 🚀 Getting Started  

### 1⃣ Prerequisites  

- **JDK 17+**  
- **Maven**  
- **MySQL & MongoDB** (Ensure both databases are running)  
- **Docker (Optional, for containerized deployment)**  

---

### 2⃣ Installation  

#### **Clone the repository**  
```sh
git clone https://github.com/yourusername/start2launch-backend.git
cd start2launch-backend
```

#### **Configure environment variables**  
Update `application.yml` with database credentials & OAuth settings.

#### **Run the application**  
```sh
mvn spring-boot:run
```

---

## 📡 API Endpoints  

| Method | Endpoint | Description | Authentication |
|--------|---------|-------------|---------------|
| POST | `/auth/register` | Register a new user | ❌ |
| POST | `/auth/login` | Authenticate user | ❌ |
| GET | `/projects` | Fetch all projects | ✅ |
| POST | `/projects` | Create a new project | ✅ (Admin/Lead) |
| GET | `/chat/messages/{projectId}` | Get messages for a project | ✅ |
| POST | `/chat/send` | Send a message | ✅ |

📌 **Full API Documentation**: [Swagger UI](http://localhost:8080/swagger-ui.html)  

---

## 🛠️ Deployment  

### Docker  
```sh
docker build -t start2launch-backend .
docker run -p 8080:8080 start2launch-backend
```

### Kubernetes  
```sh
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

---

## 📢 Contributing  

We welcome contributions! Feel free to submit issues and pull requests.  

1. Fork the repo  
2. Create a new branch (`git checkout -b feature-branch`)  
3. Commit your changes (`git commit -m "Added new feature"`)  
4. Push to the branch (`git push origin feature-branch`)  
5. Open a PR  

---

## 📚 License  

This project is licensed under the **MIT License**.  

---

🚀 **Start2Launch Backend - Powering Real-Time Collaboration!**  

