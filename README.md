# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The application listens on port 8000 inside the container (published on host port 8080) and returns a plain-text health status message.

## Verification

The running application should be verified using an HTTP request to port 8000.

## Usage

Build the image:

    docker build -t git-docker-app:test .

Run the container, mapping host port 8080 to container port 8000:

    docker run -d --name app-test -p 8080:8000 git-docker-app:test

Check the response:

    curl http://localhost:8080

Stop and remove the container:

    docker rm -f app-test
