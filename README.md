# 🚀 DevOps End-to-End Project (CI/CD + Kubernetes + Monitoring)

## 📌 Overview
This project demonstrates a complete DevOps pipeline from code to deployment using modern tools and best practices.

It includes:
- CI/CD pipeline using GitHub Actions
- Docker containerization
- Kubernetes deployment with auto-scaling
- Monitoring using Prometheus & Grafana
- Alerting using PrometheusRule

---

## 🏗️ Architecture

Code → GitHub → CI/CD → Docker → Kubernetes → Monitoring → Alerts

---

## ⚙️ Tech Stack

- CI/CD: GitHub Actions  
- Containerization: Docker  
- Orchestration: Kubernetes (k3s)  
- Monitoring: Prometheus, Grafana  
- Alerting: PrometheusRule  
- Infrastructure: Terraform (conceptual)  
- Language: Python (Flask)  

---

## 🚀 Features Implemented

### 🔹 CI/CD Pipeline
- Automated build using GitHub Actions
- Docker image build and push to Docker Hub

### 🔹 Kubernetes Deployment
- Multi-replica deployment
- Service exposure using NodePort
- Rolling updates

### 🔹 Auto Scaling
- Horizontal Pod Autoscaler (HPA)
- CPU-based scaling

### 🔹 Monitoring
- Prometheus metrics collection
- Grafana dashboards

### 🔹 Alerting
- Custom PrometheusRule
- CPU threshold alerting

---

## 🧪 Run Locally

### Build Docker Image
docker build -t devops-app ./app

### Deploy to Kubernetes
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

### Enable Auto Scaling
kubectl autoscale deployment devops-app --cpu=50% --min=2 --max=5

---

## 📈 Monitoring Setup

helm install monitoring prometheus-community/kube-prometheus-stack

kubectl port-forward svc/monitoring-grafana 3000:80

---

## 🚨 Alerting

- Custom alert for high CPU usage
- Triggered using PrometheusRule

---

## 👤 Author

Sunil Emjala  
GitHub: https://github.com/sunilemj
