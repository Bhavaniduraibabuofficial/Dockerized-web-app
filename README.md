# Dockerized Student Management Web Application

## Overview

The Dockerized Student Management Web Application is a beginner-friendly DevOps project that demonstrates how to containerize and deploy a web application using Docker. The application is built with Node.js and Express.js and serves a simple web interface developed using HTML and CSS.

The main goal of this project is to understand Docker fundamentals, including creating Docker images, running containers, and deploying applications in a consistent and portable environment. By packaging the application and its dependencies into a Docker container, the application can run reliably across different systems without requiring additional configuration.

---

## Features

- Simple web application built with Node.js and Express.js
- Static frontend using HTML and CSS
- Dockerized deployment
- Easy setup and execution
- Beginner-friendly DevOps project
- Portable and consistent runtime environment

---

## Technologies Used

- Node.js
- Express.js
- HTML5
- CSS3
- Docker
- Visual Studio Code

---

## Project Structure

```text
dockerized-web-app/
│
├── public/
│   ├── index.html
│   └── style.css
│
├── server.js
├── package.json
├── Dockerfile
└── README.md
```

---

## Prerequisites

Make sure the following software is installed on your system:

### Check Node.js

```bash
node -v
npm -v
```

### Check Docker

```bash
docker --version
```

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/dockerized-web-app.git
cd dockerized-web-app
```

### Install Dependencies

```bash
npm install
```

---

## Running the Application Locally

Start the application:

```bash
node server.js
```

Open your browser and visit:

```text
http://localhost:3000
```

---

## Docker Setup

### Build Docker Image

```bash
docker build -t student-app .
```

### Verify Image

```bash
docker images
```

---

## Run Docker Container

```bash
docker run -d -p 3000:3000 --name student-container student-app
```

### Verify Running Container

```bash
docker ps
```

---

## Access the Application

Open the following URL in your browser:

```text
http://localhost:3000
```

---

## Docker Commands

### Build Image

```bash
docker build -t student-app .
```

### Run Container

```bash
docker run -d -p 3000:3000 --name student-container student-app
```

### View Running Containers

```bash
docker ps
```

### View Container Logs

```bash
docker logs student-container
```

### Stop Container

```bash
docker stop student-container
```

### Remove Container

```bash
docker rm student-container
```

### Remove Image

```bash
docker rmi student-app
```

---

## Dockerfile

```dockerfile
FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "server.js"]
```

---

## Architecture

```text
User
  ↓
Web Browser
  ↓
localhost:3000
  ↓
Docker Container
  ↓
Node.js Express Server
  ↓
HTML + CSS Frontend
```

---

## Learning Outcomes

Through this project, I learned:

- Docker fundamentals
- Docker images and containers
- Dockerfile creation
- Containerized application deployment
- Basic DevOps workflow
- Environment consistency and portability

---

## Future Enhancements

- Student registration form
- Student records management
- MongoDB database integration
- CRUD operations
- Docker Compose support
- CI/CD pipeline using GitHub Actions
- Cloud deployment
---