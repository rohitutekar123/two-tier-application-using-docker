 # Flask App with MySQL Docker Setup

This is a simple Flask app that interacts with a MySQL database. The app allows users to submit messages, which are then stored in the database and displayed on the frontend.

## Prerequisites

efore you begin, make sure you have the following installed:

Docker & Docker Compose

Git (optional, for cloning the repository)

A remote or local server for deployment

## Setup

1️⃣ Clone the Repository

2️⃣ Create a .env file for Secure Variables

touch .env

Open .env and add:

MYSQL_HOST={}
MYSQL_USER={}
MYSQL_PASSWORD={}
MYSQL_DB={}

3️⃣ Build & Run the Application with Docker Compose

docker-compose up --build -d

The app should be running at:

Frontend: http://localhost

Backend: http://localhost:5000

4️⃣ Initialize MySQL Database

Connect to MySQL and create a table:

## Usage

1️⃣ Build the Flask Application Docker Image
2️⃣ Create a Docker Network
3️⃣ Run the MySQL Container
4️⃣ Run the Flask Application Container

🔹 CI/CD Pipeline using GitHub Actions

1️⃣ Store Secrets in GitHub

Go to GitHub → Repo Settings → Secrets → Actions, and add:

DOCKER_USERNAME → Your Docker Hub username

DOCKER_PASSWORD → Your Docker Hub password

SERVER_IP → Your server's IP address

SSH_PRIVATE_KEY → Private SSH key for server login
2️⃣ GitHub Actions Workflow (deploy.yml)


1️⃣ Store Secrets in GitHub
