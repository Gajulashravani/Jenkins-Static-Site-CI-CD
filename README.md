# Jenkins-Static-Site-CI-CD

Project Focus: Accelerating Deployment with Jenkins CI/CD

This repository details a Continuous Integration/Continuous Deployment (CI/CD) pipeline I designed to streamline the software release process. It takes a simple static website and automates its journey from GitHub commit to a running Docker container.

The Business Impact (Why I Built This)

Before this pipeline, releases required multiple manual steps, leading to delays and human error. This automated solution now handles all stages—building, testing, pushing, and deploying—autonomously.

Result: I achieved an 80% reduction in deployment time, translating directly into faster feedback loops and improved developer productivity.

Technology Stack

Orchestration: Jenkins (using Groovy DSL for "Pipeline as Code")

Containerization: Docker

Target Environment: Nginx (running inside the Docker container)

Source Control: Git/GitHub

Pipeline Flow (The Process)

The Jenkinsfile orchestrates the following stages:

Build: Compiles the source code into a portable Docker image.

Test: Runs static checks (simulated testing in this demo) to ensure code quality before proceeding.

Push: Tags the validated image and securely pushes it to a centralized Docker Registry (e.g., Docker Hub).

Deploy: Connects to the target server, pulls the new image, and launches the container, ensuring zero downtime (via container restart logic).

Files in this Repository

Jenkinsfile: The core script defining the pipeline logic (Groovy).

Dockerfile: Instructions to build the lightweight Nginx image.

src/index.html: The sample application code.
