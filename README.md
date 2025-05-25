# Role-Based Canary Deployment on EKS with Istio

This project demonstrates a role-based canary deployment strategy using AWS Elastic Kubernetes Service (EKS) and Istio. It routes traffic to different versions of a Go-based backend service based on user roles defined in HTTP headers.

## 🔧 Project Overview

- Two versions of a Go backend service (v1 and v2) are deployed in Kubernetes.
- Docker is used to containerize both versions.
- Istio service mesh enables conditional traffic routing via VirtualService and DestinationRule.
- Traffic is routed based on user roles:
  - Requests with header `role: admin` go to v2
  - All others go to v1

## 📦 Components

- `backend-v1/` – Go application version 1
- `backend-v2/` – Go application version 2
- `manifests/` – Kubernetes Deployment and Service YAMLs
- `istio-config/` – Istio Gateway, VirtualService, DestinationRule YAMLs
- `Dockerfile` – Used to build Docker images for both versions
- `diagrams/` – Architecture diagrams and request flow illustrations
