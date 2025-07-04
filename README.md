# Kubernetes Notes App Deployment

This repository contains all Kubernetes manifests and Dockerfile for deploying a full-stack Django-based Notes App using Kubernetes and Docker.

## 🚀 Project Overview

- **Backend:** Django (Python)
- **Containerization:** Docker
- **Orchestration:** Kubernetes
- **Cloud Platform:** AWS EC2 Instance

## 📁 Folder Structure

K8S-NOTES-APP-DEPLOYMENT/
├── Dockerfile # Backend container config
├── namespace.yml # Defines K8s namespace
├── deployment.yml # Deployment manifest
├── service.yml # Internal ClusterIP service
├── README.md # Project description
├── Kubernetes Deployment Documentation.md # Extended guide

bash
Copy code

## 🔧 Setup Instructions

1. **Build Docker Image**
   ```bash
   docker build -t notes-app-k8s .
   docker tag notes-app-k8s utkarsh5404/notes-app-k8s:latest
   docker push utkarsh5404/notes-app-k8s:latest
Create Namespace

bash
Copy code
kubectl apply -f namespace.yml
Deploy to Kubernetes

bash
Copy code
kubectl apply -f deployment.yml
kubectl apply -f service.yml
Access the App

bash
Copy code
kubectl port-forward service/notes-app-service -n notes-app 8000:8000
Now visit: http://localhost:8000