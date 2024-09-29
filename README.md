# My Docker Web Application

This project is a simple web application using Docker and Nginx to serve a static HTML page. It demonstrates how to create a Docker image, manage volumes, and deploy the application locally.

## Table of Contents

- [Project Setup](#project-setup)
- [Steps to Build and Run the Project](#steps-to-build-and-run-the-project)
- [Upload to GitHub](#upload-to-github)
- [Accessing the Web Application](#accessing-the-web-application)
- [Commands Summary](#commands-summary)

## Project Setup

1. **Create a Project Directory**:

Navigate to your project directory
cd ~/my-docker-web-app

Create an HTML file
echo "<h1>Hello, Docker!</h1>" > index.html

Create a Dockerfile
touch Dockerfile

Add content to Dockerfile
(use your preferred text editor)

Build the Docker image
docker build -t my-nginx .

Create a Docker volume
docker volume create web_data

 Run the Nginx container with the volume
docker run -d --name my-nginx-container -v web_data:/usr/share/nginx/html -p 8080:80 my-nginx



