# WanderQuest: Running with Docker Compose

This project consists of two services: the **NestJS** backend and the **Next.js** frontend. This README will guide you through setting up and running both services using **Docker Compose**.

## Prerequisites

Before running the Docker Compose setup, ensure that you have the following:

1. **Docker** and **Docker Compose** installed on your machine.
    - You can download Docker from [here](https://www.docker.com/products/docker-desktop).

   **Note**: You can check the README files in the backend and frontend projects for more information about the specific environment variables required for each.

## File Structure

```
wanderquest/
├── wanderquest-backend/      # NestJS backend project
│   ├── Dockerfile
│   ├── ...
├── wanderquest-frontend/     # Next.js frontend project
│   ├── Dockerfile
│   ├── ...
├── docker-compose.yml        # Docker Compose configuration file
└── README.md                 # This README file
```

## Setup and Running the Project

### Step 1: Clone the Repository

If you haven't already cloned the repository, you can do so with:

```bash
git clone https://github.com/Ali-Ak-98/wanderquest.git
cd wanderquest
```

**Important**: Be sure to review the backend and frontend README files for details on which environment variables are required for each project.

### Step 2: Build and Start the Services with Docker Compose

With Docker Compose, you can easily build and run both the backend and frontend services together.

1. **Build and start the services** by running the following command in the root directory (where the `docker-compose.yml` file is located):

   ```bash
   docker-compose up --build
   ```

   This command will:
    - Build the Docker images for both the frontend and backend services.
    - Start the containers for both services and link them via the custom `app-network` network.
    - Expose the frontend at `http://localhost:3001` and the backend at `http://localhost:3000`.

2. **Access the Services**:
    - The **Next.js frontend** will be available at `http://localhost:3001`.
    - The **NestJS backend** will be available at `http://localhost:3000`.

### Step 3: Stopping the Services

To stop the running services, use the following command:

```bash
docker-compose down
```

This will stop and remove the containers, networks, and volumes created by `docker-compose up`.

## Backend and Frontend Details

For more detailed setup instructions and information about the backend and frontend projects, please refer to the individual README files located in the following directories:

- [Backend README](./wanderquest-backend/README.md)
- [Frontend README](./wanderquest-frontend/README.md)

---
