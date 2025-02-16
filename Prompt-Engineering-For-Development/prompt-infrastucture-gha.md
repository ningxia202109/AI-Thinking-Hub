1. **Application Overview**:
   - The Python application is a REST API built with FastAPI. It uses PostgreSQL for the database and Redis for caching.
   - The application is containerized using Docker and deployed on AWS

2. **GitHub Actions CI/CD Workflow**:
   - Create a GitHub Actions workflow to:
     - Run unit tests using `pytest`.
     - Lint the code using `black` and `flake8`.
     - Build a Docker image for the FastAPI application.
     - Push the Docker image to ECR.
     - Send commit id to ArgoCD for deployment.
     - follow GitHub Actions CI/CD Workflow
   - Support multiple environments (`dev`, `staging`, `production`) using GitHub environment secrets.

3. **Exampe GitHub Actions CI/CD Workflow**:
