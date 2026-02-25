# Laravel Docker Setup 🚀

This repository contains a Laravel 10 development environment using Docker.

## 🧱 Tech Stack

- Laravel 10
- PHP
- Nginx
- MySQL 5.7
- phpMyAdmin
- Docker & Docker Compose

---

## 📦 Project Structure

```
laravel-docker/
│
├── docker-compose.yml
├── Dockerfile
├── nginx/
│   ├── default.conf
│   └── load-balancer.conf
└── src/ (Laravel Application)
```

---

## ⚙️ Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/Faraysz/laravel-docker.git
cd laravel-docker
```

### 2️⃣ Build & Run Containers

```bash
docker-compose up -d --build
```

### 3️⃣ Access Application

Laravel App:
```
http://localhost
```

phpMyAdmin:
```
http://localhost:8081
```

---

## 🛑 Stop Containers

```bash
docker-compose down
```

---

## 🔥 Features

- Multi-container architecture
- Nginx load balancer
- MySQL database container
- phpMyAdmin integration
- Clean Docker development environment

---

## 👨‍💻 Author

Faraysz
