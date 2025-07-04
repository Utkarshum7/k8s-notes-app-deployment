# Kubernetes Deployment Documentation  
**Project:** Django Notes App Deployment using Kubernetes  
**Author:** Utkarsh Amaresh  
**Date:** July 2025  
**Version:** 1.0  

---

## 1. Introduction

Kubernetes (K8s) is a powerful open-source platform for managing containerized applications in a clustered environment. It automates deployment, scaling, and management of applications.  
This documentation explains how I deployed a Django-based Notes App on a Kubernetes cluster hosted on an AWS EC2 instance, along with Docker containerization and service exposure.

---

## 2. Why Kubernetes?

Before Kubernetes, deploying with just Docker meant manual steps for container management. Kubernetes improves this by:

- Automatically managing container lifecycles
- Providing built-in **scalability**, **self-healing**, and **load balancing**
- Making deployments declarative and repeatable

---

## 3. Architecture Overview

User → Kubernetes Service → Pod (Django App Container)

yaml
Copy code

- The application backend is written in Django.
- The app is containerized using Docker and stored on Docker Hub.
- Kubernetes manages the lifecycle of this container using a Deployment.
- The Service (ClusterIP) allows internal networking between Pods.
- Port-forwarding is used to access the app from outside.

---

## 4. Tools and Technologies Used

- **Django:** Backend Framework  
- **Docker:** Containerization tool  
- **Kubernetes:** Container orchestration  
- **AWS EC2:** Hosting platform  
- **kubectl:** Kubernetes CLI  
- **Docker Hub:** Image registry  

---

## 5. File Structure
