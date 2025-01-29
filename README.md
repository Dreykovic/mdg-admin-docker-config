# Project Setup and Launch Guide

## Table of Contents

1. [Cloning the Repository](#cloning-the-repository)
2. [Setting Up Environment Variables](#setting-up-environment-variables)
3. [Building and Launching the Application](#building-and-launching-the-application)

---

## Cloning the Repository

To start working with this project, first, clone the repository to your local machine:

```bash
git clone <repository-url>
cd <repository-folder>
```

Replace `<repository-url>` with the URL of the repository and `<repository-folder>` with the name of the cloned folder.

---

## Setting Up Environment Variables

Before running the project, you need to configure the required environment variables. Follow the steps below:

1. **Server Environment Variables:**
   - Navigate to the `server` directory:
     ```bash
     cd server
     ```
   - Copy the example environment file:
     ```bash
     cp .env.server.example .env
     ```
   - Open the `.env` file in a text editor and fill in the required variables:

     ```plaintext
     # DEFAULT USER
     DEFAULT_USER_NAME=
     DEFAULT_USER_PROFILES=
     DEFAULT_USER_CONTACT=
     DEFAULT_USER_PASSWORD=
     DEFAULT_USER_EMAIL=

     # DATABASE
     DATABASE_URL=
     ```

     Ensure that all variables are correctly filled in before proceeding.

2. **Client Environment Variables:**
   - Navigate to the `client` directory:
     ```bash
     cd ../client
     ```
   - Copy the example environment file:
     ```bash
     cp .env.client.example .env
     ```
   - Open the `.env` file in a text editor and configure it as needed.

3. **Root Environment Variables:**
   - Navigate back to the root directory:
     ```bash
     cd ..
     ```
   - Copy the example environment file:
     ```bash
     cp .env.example .env
     ```
   - Open the `.env` file in a text editor and fill in any necessary variables.

---

## Building and Launching the Application

Once the environment variables are set, you can build and launch the application using Docker:

1. Build the application:
   ```bash
   docker compose build --no-cache
   ```

2. Launch the application:
   ```bash
   docker compose up
   ```

3. Open your browser and reach the localhost:4172 address to use the application

This will build and start all the services defined in the `docker-compose.yaml` file.

4. Stop Containers instances
   ```bash
   docker compose down
   ```
---

### Additional Notes
- Ensure Docker and Docker Compose are installed and running on your system before proceeding.
- Check the logs after launching to confirm that all services have started successfully.

Happy coding!
