# End-to-End DevOps Pipeline (Java + Maven + Docker + Jenkins) 🚀

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline using Jenkins, Docker, and a Java Maven application.

The pipeline automates the process of building, packaging, containerizing, and deploying the application.

---

## 🧰 Tech Stack

* Java (Maven)
* Jenkins (CI/CD)
* Docker (Containerization)
* GitHub (Source Code Management)

---

## 🔄 CI/CD Pipeline Workflow

1. Developer pushes code to GitHub
2. Jenkins pipeline is triggered automatically
3. Maven build runs inside a Docker container
4. Application JAR file is generated
5. Docker image is built using the application
6. Existing container is stopped and removed
7. New container is deployed

---

## ⚙️ Jenkins Pipeline Stages

### 1️⃣ Build Maven (Docker Agent)

* Uses Maven Docker image
* Runs `mvn clean package`
* Ensures consistent build environment

### 2️⃣ Build Docker Image

* Creates Docker image from Dockerfile

### 3️⃣ Deploy Container

* Removes existing container (if any)
* Runs new container with latest image

---

## 🐳 Docker Commands

### Build Image

```bash
docker build -t my-app .
```

### Run Container

```bash
docker run -d -p 8081:8080 --name my-app-container my-app
```

---

## 📂 Project Structure

```
.
├── src/                # Java source code
├── pom.xml             # Maven configuration
├── Dockerfile          # Docker image setup
├── Jenkinsfile         # CI/CD pipeline definition
├── README.md           # Project documentation
```

---

## 🚀 How to Run Locally

### Step 1: Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### Step 2: Build Application

```bash
mvn clean package
```

### Step 3: Build Docker Image

```bash
docker build -t my-app .
```

### Step 4: Run Container

```bash
docker run -d -p 8081:8080 my-app
```

---

## 🔥 Key Highlights

* CI/CD pipeline using Jenkins
* Maven build inside Docker container
* Automated Docker image creation
* Zero-downtime container redeployment
* Real-world DevOps workflow implementation

---

## 👨‍💻 Author

Vishwas Magar

---
