# CI/CD Pipeline with GitHub Actions & Docker
This project demonstrates a full CI/CD pipeline using **GitHub Actions** and **Docker**, targeting a Python Django web application. The pipeline automatically builds and deploys the app whenever changes are pushed to the `main` branch.

## Tools Used

- **GitHub Actions** – for automating CI/CD
- **Docker & DockerHub** – for containerization and image registry
- **Python Django** – web framework used in the application
- **Localhost** – environment for running the container

## Steps Involved in Building the Project

### 🔧 Developed the Django App

- Created views and URL configurations
- Enabled app routing via `views.py`, `urls.py`
- Generated `requirements.txt` with Django dependency

### 🐳 Dockerized the Application

- Created a `Dockerfile` with required instructions to build the Django app image

### ⚙️ Created GitHub Actions Workflow

Workflow path: `.github/workflows/docker-ci-cd.yml`

Steps include:
- Code checkout
- Docker Hub authentication using secrets
- Docker image build and push

### 🔐 Configured GitHub Secrets

- `DOCKER_USERNAME` – your Docker Hub username
- `DOCKER_PASSWORD` – your Docker Hub password or token

## Push Code to GitHub Repo
![](https://github.com/deepakbehera11/Ci-Cd-Pipeline-with-Github-Actions-and-docker/blob/ca3ea56352b19df767d527ef53c95571571d1a0e/assets/Screenshot-Github-Actions.png)

## 🐳 Docker Image Management

### 🔽 Pulled the Docker Image Locally

```bash
docker pull deepak171/djangoapp:latest
```
![](https://github.com/deepakbehera11/Ci-Cd-Pipeline-with-Github-Actions-and-docker/blob/ca3ea56352b19df767d527ef53c95571571d1a0e/assets/Screenshot-docker-pull.png)

### 🔽 Run the Image
```bash
docker run -p 8080:8080 deepak171/djangoapp
```
![](https://github.com/deepakbehera11/Ci-Cd-Pipeline-with-Github-Actions-and-docker/blob/ca3ea56352b19df767d527ef53c95571571d1a0e/assets/Screenshot-docker-run.png)

![](https://github.com/deepakbehera11/Ci-Cd-Pipeline-with-Github-Actions-and-docker/blob/ca3ea56352b19df767d527ef53c95571571d1a0e/assets/Screenshot-docker-ps.png)

#### The application will be accessed when we give `/demo` after the URL because it's the context root of the django application
![](https://github.com/deepakbehera11/Ci-Cd-Pipeline-with-Github-Actions-and-docker/blob/484ae55082c02c8410e1c052e33fab35d5655e21/assets/Screenshot-djagoapp.png)


