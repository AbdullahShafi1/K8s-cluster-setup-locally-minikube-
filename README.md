# K8s-cluster-setup-locally-minikube

This repository contains a simple web application deployed on a Kubernetes cluster using Minikube. It serves as a practice setup for Kubernetes clusters. The setup consists of two containers (1 replica each) running locally with Minikube and Docker drivers.

## Description

The deployment is designed to run a web application that interacts with a MongoDB database. It uses Kubernetes to manage the containers and services in a local environment.

### Technologies Used:
- **Minikube**: A local Kubernetes setup using Docker drivers.
- **Kubernetes**: For orchestration of the containers.
- **Docker**: Container runtime used with Minikube.
- **MongoDB**: Used as the database for the web app.
- **Node.js**: Web application running on port 3000.
  
### Architecture

This setup includes two containers:
1. **Webapp Container**: A Node.js web application that connects to MongoDB for data storage.
2. **MongoDB Container**: A MongoDB instance that stores data for the web application.

Each container has a corresponding service connected to the Kubernetes API server, allowing seamless communication between the web app and the database.

### Kubernetes Resources
1. **Deployment**:
   - **Webapp Deployment**: A single replica of the web application.
   - **MongoDB Deployment**: A single replica of the MongoDB database.
2. **Services**:
   - **Webapp Service**: Exposes the web application via a NodePort.
   - **MongoDB Service**: Exposes the MongoDB database on the internal Kubernetes network.


