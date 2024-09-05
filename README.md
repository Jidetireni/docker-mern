# MERN Stack Docker Setup

This repository contains a `Makefile` for managing a Docker-based setup for a
MERN (MongoDB, Express, React, Node.js) stack application. The setup includes Docker
containers for the frontend, backend, and MongoDB services, along with a Docker network and volume configuration.

## Prerequisites

- Docker
- Docker Compose
- Make (optional, but recommended for using the provided `Makefile`)

## Setup

### **1. Clone the Repository**

To use this Docker project, clone the repository:

```bash
git clone https://github.com/balavi7/MERN-Docker-Compose.git
```

Update the `Dockerfile` and `docker-compose.yml` files to match the respective directories for your frontend and backend services.

### **2. Build Docker Images**

To build Docker images for the frontend and backend services, run:

```bash
make build
```

### **3. Create Docker Network**

To create a Docker network named `mern`, run:

```bash
make network
```

### **4. Create Docker Volume**

To create a Docker volume named `mongodb-data` for MongoDB data persistence, run:

```bash
make volume
```

### **5. Run Containers**

To start the Docker containers for the frontend, backend, and MongoDB services, run:

```bash
make run
```

- **Frontend**: Accessible on port `5173`
- **Backend**: Accessible on port `5050`
- **MongoDB**: Accessible on port `27017`

### **6. View Running Containers**

To list the currently running Docker containers, run:

```bash
make ps
```

### **7. View Docker Images**

To list all Docker images, run:

```bash
make images
```

### **8. Remove Containers**

To remove the running Docker containers, run:

```bash
make rm
```

### **9. Stop Containers**

To stop the running Docker containers, run:

```bash
make stop
```

### **10. Docker Compose Commands**

You can also use Docker Compose for managing your containers:

- To start all services defined in a `docker-compose.yml` file:

  ```bash
  make up
  ```

- To stop all services defined in a `docker-compose.yml` file:

  ```bash
  make down
  ```

## Notes

- The `mongodb-data` volume is used for MongoDB data persistence. If you want to use a local directory for MongoDB data, modify the `docker run` command in the `run` section of the `Makefile` accordingly.
- Ensure that Docker and Docker Compose are properly installed and running on your system.
