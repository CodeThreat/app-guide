---
description: >-
  This guide provides a step-by-step walkthrough for deploying the CodeThreat
  ASP with MongoDB using Docker Compose.
---

# Deploy with Docker

### Access to CodeThreat Container Registry

The CodeThreat container registry is private and accessible only upon request. To deploy CodeThreat ASP, you’ll need an access token and login credentials, which will be provided to you by the CodeThreat team.

Once you receive your credentials, follow these steps to log in to our container registry:

```bash
docker login codethreatcontainer.azurecr.io
```

Enter the provided **username** and **access token** when prompted. This will grant you access to download the CodeThreat ASP Docker images.

### Step 1: Create the Docker Compose File

Create a file named `docker-compose.yaml` in your deployment directory and add the following content:

```yaml
version: "3"

services:
  codethreat_asp:
    image: codethreatcontainer.azurecr.io/codethreatsast-server-selfhosted:2411.07.1-master
    restart: on-failure
    ports:
      - "8081:8081" # Expose the application on port 8081
    depends_on:
      - mongodb
    volumes:
      - ./ctdata:/app/ctdata
    environment:
      HOSTNAME: "0.0.0.0"
      PORT: "8081"
      MONGO_URL: "mongodb://mongodb:27017"
      # Uncomment and configure SSL settings if needed
      # SECURE_PORT: "443"
      # CERTIFICATE_KEY_PATH: "/path/to/key.key"
      # CRT_PATH: "/path/to/cert.crt"

  mongodb:
    image: mongo
    restart: always
    volumes:
      - ./mongodb/data:/data/db

```

### Step 2: Start the Containers

Run the following command to start the services in detached mode:

```bash
docker-compose up -d
```
