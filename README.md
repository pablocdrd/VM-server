# DevOps Homelab

Personal DevOps homelab built to gain hands-on experience with Linux system administration,
containerization, and basic infrastructure concepts.

This project is continuously evolving and used as a learning and experimentation environment.

---

## 🚀 Goals
- Learn and practice Linux administration
- Understand Docker and container-based workflows
- Implement a reverse proxy for service exposure
- Add basic monitoring and observality
- Build a foundation for future multi-node and networking setups

---

## 🧱 Stack
- Ubuntu Linux (Virtual Machine)
- Docker & Docker Compose
- Nginx Proxy Manager (Reverse Proxy)
- Portainer (Container Management)
- Test services (e.g. whoami)
- Uptime Kuma (Monitoring)

---

## 🏗️ Architecture
- Ubuntu VM running Docker as the host system
- Nginx Proxy Manager handling incoming HTTP traffic
- Portainer used to manage and monitor containers
- Services exposed internally through the reverse proxy
- Uptime Kuma (Monitoring)

---

## 📁 Project Structure
```text
VM-server/
├── stacks/
│   ├── core/
│   │   └── docker-compose.yml
│   ├── npm/
│   │   └── docker-compose.yml
│   └── monitoring/
│       └── uptime-kuma/
│           └── docker-compose.yml
├── .gitignore
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

cd ../monitoring/uptime-kuma
docker-compose up -d

### Stop
cd npm
docker compose down

cd ../stacks/core
docker compose down

cd ../monitoring/uptime-kuma
docker-compose down

## Configuration
Environment variables should be stored in a local .env file (not committed).
See .env.example for reference.

## Security
- Secrets are not committed to the repository (see .gitignore and .env.example)
- This homelab is intended for private/internal network usage

```
## 📚 What I learned

- Setting up and operating Dockerized services on a Linux VM  
- Using a reverse proxy (Nginx Proxy Manager) to expose internal services  
- Managing containers and stacks with Portainer  
- Implementing basic service monitoring and observability with Uptime Kuma  
- Understanding the importance of uptime, response time and early failure detection  
- Documenting infrastructure and services for reproducibility  
