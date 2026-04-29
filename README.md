# Secure Zomato Clone Deployment with DevSecOps CI/CD

## Project Overview

This project demonstrates a secure CI/CD deployment workflow for a Zomato-inspired React frontend application.

The application is containerized using Docker and deployed through a Jenkins declarative pipeline. The pipeline includes code build, SonarQube code quality analysis, OWASP Dependency Check, Trivy vulnerability scanning, Docker image build, Docker Hub push, and container deployment on AWS EC2.

## Tech Stack

- React.js
- Jenkins
- Docker
- Docker Hub
- SonarQube
- Trivy
- OWASP Dependency Check
- AWS EC2 Ubuntu 22.04
- Nginx

## Architecture

Developer pushes code to GitHub.

Jenkins pulls the latest code from GitHub.

Jenkins installs dependencies and builds the React application.

SonarQube checks code quality.

OWASP Dependency Check scans project dependencies.

Trivy scans the file system and Docker image for vulnerabilities.

Docker builds the application image.

Docker image is pushed to Docker Hub.

Jenkins deploys the final container on AWS EC2.

## CI/CD Pipeline Stages

1. Checkout source code
2. Install npm dependencies
3. Build React application
4. SonarQube analysis
5. OWASP Dependency Check
6. Trivy filesystem scan
7. Docker image build
8. Trivy Docker image scan
9. Docker image push to Docker Hub
10. Deploy container on EC2

## Ports Used

| Service | Port |
|---|---|
| Jenkins | 8080 |
| SonarQube | 9000 |
| Zomato App | 3000 |
| SSH | 22 |

## How to Run Locally

```bash
npm install
npm run build
