# 🚀 GitHub Actions Demo — Production-Style CI/CD Pipeline

A production-style **three-tier application** with a full CI/CD pipeline implemented using **GitHub Actions**. This project demonstrates an end-to-end DevOps workflow including code versioning, automated builds, testing, and deployment across frontend, backend, and database layers.

---

## 📁 Project Structure

```
github-actions-demo/
├── .github/
│   └── workflows/        # GitHub Actions CI/CD pipeline definitions
├── frontend/             # Frontend application (CSS, JavaScript, HTML)
├── backend/              # Backend application (Go)
├── mysql/                # Database configuration and migrations
├── nginx/                # Nginx reverse proxy configuration
├── .env.example          # Environment variable template
└── docker-compose.yml    # Multi-container Docker setup
```

---

## 🛠️ Tech Stack

| Layer      | Technology                  |
|------------|-----------------------------|
| Frontend   | HTML, CSS, JavaScript       |
| Backend    | Go                          |
| Database   | MySQL                       |
| Proxy      | Nginx                       |
| Container  | Docker / Dockerfile         |
| CI/CD      | GitHub Actions              |

---

## ⚙️ CI/CD Pipeline

The pipeline is defined in `.github/workflows/` and automates the following:

- ✅ **Code Checkout** — Pull the latest code on every push or pull request
- 🔨 **Build** — Build frontend and backend services
- 🧪 **Test** — Run automated tests across all layers
- 🐳 **Docker Build & Push** — Build Docker images and push to Docker Hub
- 🚀 **Deploy** — Deploy the full stack using Docker Compose

---

## 🚦 Getting Started

### Prerequisites

- [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- [Go](https://golang.org/) (for local backend development)
- A Docker Hub account (for image publishing)

### 1. Clone the Repository

```bash
git clone https://github.com/faizcodingc/github-actions-demo.git
cd github-actions-demo
```

### 2. Configure Environment Variables

```bash
cp .env.example .env
# Edit .env with your configuration
```

### 3. Run Locally with Docker Compose

```bash
docker-compose up --build
```

The application will be accessible via Nginx at `http://localhost`.

---

## 🔐 GitHub Secrets Required

To enable Docker Hub publishing in the CI/CD pipeline, add these secrets to your GitHub repository (`Settings → Secrets and variables → Actions`):

| Secret Name         | Description                  |
|---------------------|------------------------------|
| `DOCKER_USERNAME`   | Your Docker Hub username     |
| `DOCKER_PASSWORD`   | Your Docker Hub password/token |

---

## 👥 Contributors

- **Faiz Ansari** ([@faizcodingc](https://github.com/faizcodingc))
---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> Built to demonstrate real-world DevOps practices using GitHub Actions, Docker, and a multi-tier application architecture.
