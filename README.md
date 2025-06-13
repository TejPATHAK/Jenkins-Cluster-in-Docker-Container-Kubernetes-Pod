# 🚀 Jenkins Cluster in Docker Container & Kubernetes Pod

## 📌 Objective
To build a complete **Jenkins CI/CD Cluster** using:
- Custom-built Jenkins Master and Agent Docker images (no pre-created images)
- Kubernetes Pods for Jenkins Master and Agents
- GitHub integration for job execution
- Manual node management (Cloud/Agent setup)

---

## 📦 Project Structure

jenkins-k8s-cluster/
├── jenkins-master/
│ └── Dockerfile
├── jenkins-agent/
│ ├── Dockerfile
├── k8s-yamls/
│ ├── jenkins-master-deployment.yaml
│ ├── jenkins-agent-deployment.yaml
│ └── jenkins-service.yaml


---

## 🛠️ Setup Overview

### 🔧 Jenkins Master (Docker + Kubernetes)
- Built with Rocky Linux base image
- Jenkins WAR downloaded manually
- Deployed in Kubernetes using `jenkins-master-deployment.yaml`
- Exposed on `NodePort`

### 🤖 Jenkins Agent
- Custom Dockerfile created for agent
- Deployed via `jenkins-agent-deployment.yaml`
- Connected manually using WebSocket and `agent.jar`

### 🌐 Jenkins Service
- `NodePort` service exposes Jenkins UI
- Accessed via:  
```
http://<minikube-ip>:<nodePort>
```

---

## 🚦 Pipeline Execution
- Created freestyle job in Jenkins UI
- Used agent label for job assignment
- Job executed successfully via Jenkins Agent pod

---

## ✅ Results
- Jenkins UI launched from Kubernetes
- Jenkins Agent successfully connected
- Job build completed on agent container

---

## 👨‍💻 Author
**Tejaswi Pathak**  
GitHub: [TejPATHAK](https://github.com/TejPATHAK)

---

