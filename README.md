# Dockerized Static Web Application with Jenkins CI/CD

## Overview

This project demonstrates the deployment of a static web application using Docker, Nginx, Jenkins, and Docker Hub. The application is containerized and automatically built and pushed to Docker Hub through a Jenkins CI/CD pipeline.

## Technologies Used

* HTML
* CSS
* JavaScript
* Docker
* Nginx
* Jenkins
* Docker Hub
* GitHub

## Project Architecture

GitHub Repository → Jenkins Pipeline → Docker Image Build → Container Deployment → Docker Hub

## Features

* Static website hosted using Nginx
* Dockerized application deployment
* Automated CI/CD pipeline using Jenkins
* Automatic Docker image creation
* Automatic image push to Docker Hub
* Source code version control using GitHub

## Jenkins Pipeline Stages

### 1. Clone Repository

The pipeline pulls the latest source code from the GitHub repository.

### 2. Build Docker Image

A Docker image is created using the Dockerfile present in the project.

```bash
docker build -t <image-name> .
```

### 3. Create Container

A container is created and executed from the generated Docker image.

```bash
docker run -d -p 80:80 <image-name>
```

### 4. Push Image to Docker Hub

The generated Docker image is pushed automatically to Docker Hub.

```bash
docker push <dockerhub-username>/<image-name>
```

## Dockerfile

```dockerfile
FROM nginx:alpine

COPY . /usr/share/nginx/html/

EXPOSE 80
```

## Project Structure

```text
├── css/
├── fonts/
├── images/
├── js/
├── index.html
├── news-detail.html
├── Dockerfile
└── Jenkinsfile
```

## How to Run Locally

### Build Image

```bash
docker build -t static-web-app .
```

### Run Container

```bash
docker run -d -p 8080:80 static-web-app
```

### Access Application

```text
http://localhost:8080
```

## Jenkins Pipeline Result

The Jenkins pipeline successfully performs:

* Repository cloning
* Docker image building
* Container creation
* Docker image push to Docker Hub

## Learning Outcomes

* Containerization using Docker
* Web hosting using Nginx
* CI/CD automation with Jenkins
* Docker Hub integration
* Automated deployment workflows

## Screenshots
* Build success
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/3950849d-e729-470b-80e7-3150104cce18" />
* Docker images and running container
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/0b434e82-8031-4a49-aa87-1eee3b90e622" />
* Final application
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/a5520c7c-4ff7-4b28-a99e-b1bee1d18ef7" />


## Author

Monish S
