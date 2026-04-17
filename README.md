# Kubernetes GitOps Demo (Docker + Helm + ArgoCD)

## 🚀 Overview
This project demonstrates an end-to-end GitOps-based deployment pipeline using:

- Docker (containerization)
- Kubernetes (orchestration)
- Helm (packaging)
- ArgoCD (GitOps continuous delivery)

---

## 🧱 Architecture
App → Docker → Kubernetes → Helm → ArgoCD

---

## 🔧 Steps

### 1. Build Docker Image
docker build -t <your-dockerhub>/flask-app:v1 ./app
docker push <your-dockerhub>/flask-app:v1

---

### 2. Deploy with Helm
helm install flask-app ./helm/flask-chart

---

### 3. Deploy via ArgoCD
kubectl apply -f argocd/application.yaml

---

## 🔁 GitOps Flow
- Code changes pushed to Git
- ArgoCD detects changes
- Automatically syncs with Kubernetes cluster

---

## 🎯 Key Features
- Declarative deployments
- Automated sync using ArgoCD
- Parameterized configs using Helm
- Scalable Kubernetes deployment

---

## 📌 Future Improvements
- Add Ingress
- Add CI pipeline (GitHub Actions)
- Add monitoring (Prometheus + Grafana)