# DevOps Homelab

Personal DevOps homelab built to gain hands-on experience with Linux system administration,
containerization, and basic infrastructure concepts.

This project is continuously evolving and used as a learning and experimentation environment.

---

## 🚀 Goals
- Learn and practice Linux administration
- Understand Docker and container-based workflows
- Implement a reverse proxy for service exposure
- Build a foundation for future multi-node and networking setups

---

## 🧱 Stack
- Ubuntu Linux (Virtual Machine)
- Docker & Docker Compose
- Nginx Proxy Manager (Reverse Proxy)
- Portainer (Container Management)
- Test services (e.g. whoami)

---

## 🏗️ Architecture
- Ubuntu VM running Docker as the host system
- Nginx Proxy Manager handling incoming HTTP traffic
- Isolated Docker networks for services
- Portainer used to manage and monitor containers
- Services exposed internally through the reverse proxy

---

## 📁 Project Structure
```text
devops-homelab/
├── docker-compose.yml
├── services/
│   └── whoami/
│       └── docker-compose.yml
├── nginx-proxy-manager/
│   └── docker-compose.yml
├── scripts/
│   └── start.sh
└── README.md

---

## How to run

### Requirements
- Docker installed
- Docker Compose installed

### Start
Run each stack from its folder:

cd npm
docker compose up -d

cd ../stacks/core
docker compose up -d

### Stop
cd npm
docker compose down

cd ../stacks/core
docker compose down

## Configuration
Environment variables should be stored in a local .env file (not committed).
See .env.example for reference.

## Security
- Secrets are not committed to the repository (see .gitignore and .env.example)
- This homelab is intended for private/internal network usage
