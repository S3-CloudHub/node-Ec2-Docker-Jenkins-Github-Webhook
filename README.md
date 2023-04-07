# node-todo-cicd

Run these commands:


`sudo apt install nodejs`


`sudo apt install npm`


`npm install`

`node app.js`

<h1>Deploying a Node.js Application on EC2 using GitHub, Jenkins, Docker, and Webhooks</h1>
This repository contains a Node.js application that is deployed on an EC2 instance using GitHub, Jenkins, Docker, and webhooks. The application is a simple "Hello, World!" web server that listens on port 8080.

Prerequisites
Before you can deploy this application, you will need the following:

An AWS account with an EC2 instance running Ubuntu 18.04 or later
Docker and Docker Compose installed on the EC2 instance
A GitHub account with a repository containing this application's source code
Jenkins installed and configured on the EC2 instance
A Jenkins job that pulls the latest code from the GitHub repository, builds a Docker image, and deploys the image on the EC2 instance
Setup
To set up this application for deployment on your own EC2 instance, follow these steps:

Clone this repository to your local machine: git clone https://github.com/your-username/node-app.git
Push the code to your own GitHub repository: git remote set-url origin https://github.com/your-username/node-app.git
Set up a webhook in your GitHub repository that triggers a Jenkins job whenever new code is pushed to the repository.
Set up a Jenkins job that performs the following steps:
Pull the latest code from the GitHub repository
Build a Docker image of the application using the Dockerfile in the repository
Push the Docker image to Docker Hub or your own private Docker registry
SSH into the EC2 instance and pull the latest Docker image
Stop and remove any existing Docker containers running the application
Start a new Docker container with the latest image
Test the application by accessing it on the EC2 instance's public IP address or domain name.
Configuration
This repository contains a docker-compose.yml file that defines the Docker container that runs the application. The container is configured to listen on port 8080, which is the port that the application listens on.

You can modify the docker-compose.yml file to change the container's configuration, such as the port number, environment variables, or Docker image name.

Troubleshooting
If you encounter any issues with deploying the application, you can check the Jenkins job console output for error messages. You can also SSH into the EC2 instance and check the Docker logs for the running container to see if there are any error messages.

License
This project is licensed under the MIT License - see the LICENSE file for details.




