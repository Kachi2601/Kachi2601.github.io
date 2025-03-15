
Portfolio Dockerization with GitHub Actions

Overview

This project takes my existing web portfolio and containerizes it using Docker, automating the build and deployment process with GitHub Actions. The final Docker image is pushed to Docker Hub for easy deployment.

Technologies Used
	•	Docker – To create a containerized version of the portfolio
	•	GitHub Actions – For CI/CD automation
	•	VS Code – Used for local development
	•	HTML, CSS, Java – The original web portfolio stack

Project Structure

├── .github/workflows/   # GitHub Actions pipeline
├── Dockerfile           # Docker configuration
├── src/                 # Web portfolio source files
└── README.md            # Project documentation

Setup & Usage

1. Clone the Repository


2. Build and Run the Docker Container Locally

Before setting up the GitHub Actions workflow, I tested the Docker build and run process locally:

docker build -t portfolio .
docker run -p 8080:80 portfolio

Once running, the portfolio can be accessed at http://localhost:8080.

3. GitHub Actions & Docker Hub Deployment
	•	On each push, GitHub Actions automatically builds the Docker image and pushes it to Docker Hub.
	•	I used repository secrets (DOCKER_USERNAME, DOCKER_PASSWORD) to securely authenticate with Docker Hub.
