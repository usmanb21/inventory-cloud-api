# Kubernetes Deployment – Inventory API

## 🚀 Overview
This project demonstrates deploying a containerized ASP.NET Core API to Kubernetes.

The focus is on Kubernetes architecture, networking, and exposing services using NGINX Ingress with a custom domain.

---

## 🛠️ Tech Stack
- Kubernetes
- Docker
- NGINX Ingress Controller
- ASP.NET Core API (external image)
- SQL Server

---

## ⚙️ Features
- Deployment and Pod management
- Service configuration (ClusterIP / NodePort)
- Ingress routing with custom domain (`inventory.local`)
- Port-forwarding for local testing
- API exposure through NGINX

---

## 🌐 Architecture

Client → Ingress → Service → Pod → API → Database

---

## 📦 How to Run

Apply Kubernetes manifests:

kubectl apply -f manifests/

Port forward Ingress controller:

kubectl port-forward -n ingress-nginx svc/ingress-nginx-controller 8080:80

---

## 🔗 Access

API:
http://inventory.local/api/products

Swagger:
http://inventory.local/swagger

---

## 💡 What I Learned
- Kubernetes resource management
- Service discovery and networking
- Ingress configuration and routing
- Debugging real deployment issues
- Container orchestration basics

---

## 📌 Note
This repository focuses only on Kubernetes deployment.
The API implementation is available in a separate repository.
