
```
# 🐳 My Docker Space  
**Author:** [Panchikagupta05](https://github.com/Panchikagupta05)
**Description:** A collection of Docker-based projects and experiments demonstrating containerization concepts, machine learning deployments, database integrations, networking, and cloud operations.

---

## 📦 Repository Overview

This repository serves as a structured archive of Docker experiments and application prototypes. Each folder represents a standalone project that highlights specific use cases in software development, DevOps, and cloud-native deployment.

---

## 🧪 Experiments & Projects

Below is a list of the key projects included in this repository:

### 1. 🔷 **Streamlit Spiral Visualization**
- **Description:** A Streamlit-based application that visualizes interactive spiral patterns.
- **Tech Stack:** Python, Streamlit, Docker
- **Run Command:**
  ```bash
  docker build -t streamlit-spiral .
  docker run -p 8501:8501 streamlit-spiral
  ```

---

### 2. 🔷 **Binary Classification WebApp**
- **Description:** A machine learning web application using logistic regression, built with Streamlit.
- **Tech Stack:** Python, scikit-learn, Streamlit, Docker
- **Run Command:**
  ```bash
  docker build -t binary-classifier .
  docker run -p 8501:8501 binary-classifier
  ```

---

### 3. 🔷 **Python Logging with Docker**
- **Description:** Demonstrates best practices for handling logging in a Dockerized Python environment.
- **Tech Stack:** Python, Logging module, Docker
- **Run Command:**
  ```bash
  docker build -t python-logging .
  docker run python-logging
  ```

---

### 4. 🔷 **Streamlit + PostgreSQL Integration**
- **Description:** A full-stack setup connecting a Streamlit frontend with a PostgreSQL database inside Docker containers.
- **Tech Stack:** Python, Streamlit, PostgreSQL, Docker Compose

---

### 5. 🔷 **MySQL Docker Container**
- **Description:** A standalone MySQL database container setup with connectivity support for external applications.
- **Tech Stack:** MySQL, Docker

---

### 6. 🔷 **Docker Network Experiment**
- **Description:** An experiment to understand container communication across networks using bridge and overlay drivers.
- **Tech Stack:** Docker networking, Multi-container communication

---

### 7. 🔷 **ML Model Deployment with Evidently**
- **Description:** Deploys a machine learning model alongside Evidently AI for monitoring and reporting model performance.
- **Tech Stack:** Python, Evidently, Docker

---

### 8. 🔷 **Deploying on AWS EC2**
- **Description:** Guide and setup for deploying Dockerized applications on AWS EC2 instances using the AWS CLI.
- **Tech Stack:** Docker, AWS CLI, EC2

---

### 9. 🔷 **Minikube with Docker**
- **Description:** Demonstrates running Kubernetes locally with Minikube and Docker as the container runtime.
- **Tech Stack:** Minikube, Docker, Kubernetes

---

### 10. 🔷 **Docker Bake Implementation**
- **Description:** Uses Docker Bake for building and managing multiple Docker targets with a single command.
- **Tech Stack:** Docker, docker-bake.hcl

---

## 📚 Prerequisites

Ensure the following tools are installed before running any project:

- Docker → `docker --version`
- Python → Required for ML and Streamlit apps
- AWS CLI → Required for cloud deployment

---

## 🚀 Purpose

This repository is a personal initiative to explore Docker and its ecosystem in practical scenarios. It's intended as a reference for developers and students looking to gain hands-on experience with containerized applications.

---

**Happy Containerizing!** 🐳
```
