# Hermes Monorepo

This repository contains the backend and frontend code for Hermes, a chat-based application. The backend is built using Python (FastAPI), and the frontend is built using React and TypeScript. The application is deployed with Docker Compose, ensuring an easy and consistent development and deployment process.

## Table of Contents

- Project Structure
- Requirements
- Setup Instructions
  - 1. Clone the Repository
  - 2. Environment Variables
  - 3. Build and Run with Docker Compose
  - 4. Accessing the Application
- Deployment
- Contact

## Project Structure

.
├── backend             # Backend service (FastAPI)
│   ├── app             # Application source code
│   ├── example.env     # Example environment variables file for backend
│   ├── Dockerfile      # Dockerfile for backend
│   └── requirements.txt# Python dependencies
│
├── frontend            # Frontend service (React + TypeScript)
│   ├── src             # Frontend source code
│   ├── Dockerfile      # Dockerfile for frontend
│   └── .env.example    # Example environment variables file for frontend
│
├── docker-compose.yml  # Docker Compose configuration file
└── README.md           # This file

## Requirements

- Docker
- Docker Compose

## Setup Instructions

### 1. Clone the Repository

```shell
git clone https://github.com/ishantd/hermes.git
cd hermes
```

### 2. Environment Variables

- **Backend**: Copy the `example.env` file in the `backend` directory and rename it to `.env`. Modify the values as necessary.
    
    ```shell
    cp backend/example.env backend/.env
    ```

### 3. Build and Run with Docker Compose

To build and start the services, run:

```shell
docker compose up --build
```

This will start the backend, frontend, and PostgreSQL database services.

### 4. Accessing the Application

- **Backend API**: http://<your-server-ip>:8001
- **Frontend WebApp**: http://<your-server-ip>:3001

Replace `<your-server-ip>` with your server's IP address or `localhost` if running locally.

## Deployment

To deploy this application on a remote server:

1. Ensure Docker and Docker Compose are installed on the server.
2. Clone this repository to the server.
3. Follow the Setup Instructions.
4. Update your DNS settings to point to your server's IP address.
5. Use a reverse proxy like Nginx to route traffic to the appropriate ports, or modify the Docker Compose file to expose the services on standard HTTP/HTTPS ports.

## Contact

If you have any questions or need further assistance, feel free to contact:

- **API**: https://hermes-api.ishantdahiya.com
- **WebApp**: https://hermes.ishantdahiya.com
- **GitHub Repositories**:
  - Backend: https://github.com/ishantd/hermes-backend
  - Frontend: https://github.com/ishantd/hermes-frontend
  - Monorepo: https://github.com/ishantd/hermes
- **Demo**: [Loom Video](https://www.loom.com/share/8ff83510a2494903936eb13639077bf2?sid=9f32d5ea-c101-4804-a9c0-0d42fe692696)
- **Email**: ishantdahiya@gmail.com