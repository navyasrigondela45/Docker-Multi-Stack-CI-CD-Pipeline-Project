# Docker Multi-Stack CI/CD Pipeline Project

## Project Overview

This project demonstrates a Jenkins CI/CD pipeline that dynamically builds and deploys multiple Docker-based technology stacks from a single GitHub repository using parameterized builds.

The repository contains separate folders for different technology stacks and optimized Dockerfiles for each stack.

---

## Tech Stacks Included

- HTTPD
- NGINX
- Java
- MySQL
- Node.js
- Python

---

## Project Features

### Parameterized Jenkins Pipeline

The Jenkins pipeline uses parameters to dynamically select the required application stack.

---

### Dynamic Docker Build

The pipeline automatically changes directory based on selected parameter and builds the Docker image.

```groovy
cd ${TECH_STACK}
docker build -t $image_name -f Dockerfile.v2 .
```

---

### DockerHub Integration

Integrated Jenkins with DockerHub registry for:

- Docker image tagging
- Secure Docker login using Jenkins credentials
- Docker image push to DockerHub

---

### Automated Container Deployment

The pipeline deploys containers automatically after successful image push.

---

## Repository Structure

```text
Dockerfile-Creation-And-Image-Optimization/
│
├── httpd/
├── nginx/
├── java/
├── mysql/
├── nodejs/
└── python/
```

## Outputs Included

This repository also contains output screenshots for:

- Jenkins Stage View
  <img width="1600" height="790" alt="image" src="https://github.com/user-attachments/assets/c456a146-6b8d-4721-99f3-bbc153212aa5" />

- Successful Parameterized Builds
  <img width="1600" height="786" alt="image" src="https://github.com/user-attachments/assets/6dd15cc1-e67e-4793-b6c3-4ae72abc33dd" />

- Docker Image Build Logs
  
  <img width="596" height="205" alt="image" src="https://github.com/user-attachments/assets/a2c56e2a-bea4-4e6d-ac5b-b3c926429eec" />

- DockerHub Push Output
  <img width="959" height="471" alt="image" src="https://github.com/user-attachments/assets/cd1d3dc8-8118-4a40-a0ea-c0fd8385b5cb" />

- Running Containers
  <img width="930" height="86" alt="image" src="https://github.com/user-attachments/assets/135f7168-5fed-4747-96ec-23169c3a34bc" />

- GitHub Repository Folder Structure
  <img width="1600" height="789" alt="image" src="https://github.com/user-attachments/assets/ab4441d8-0649-40eb-9a8d-96a7b35cbb00" />

---

## Skills Demonstrated

- Jenkins Declarative Pipelines
- Docker Image Optimization
- DockerHub Integration
- Parameterized Builds
- CI/CD Automation
- Multi-Stack Containerization
- GitHub Repository Structuring
- Docker Container Deployment

---

## Sample Workflow

```text
Select Stack → Pull GitHub Code → Build Docker Image → Push to DockerHub → Run Container
```
