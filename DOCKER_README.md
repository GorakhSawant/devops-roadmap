# Docker - From Beginner to Advanced 🐳

## Table of Contents
1. [Introduction to Docker](#introduction-to-docker)
2. [Installation & Setup](#installation--setup)
3. [Docker Fundamentals](#docker-fundamentals)
4. [Working with Containers](#working-with-containers)
5. [Docker Images](#docker-images)
6. [Dockerfile](#dockerfile)
7. [Docker Compose](#docker-compose)
8. [Docker Networking](#docker-networking)
9. [Docker Volumes](#docker-volumes)
10. [Docker Security](#docker-security)
11. [Docker in Production](#docker-in-production)
12. [Best Practices](#best-practices)

## Introduction to Docker
### What is Docker?
- Containerization platform
- Difference between containers and VMs
- Docker architecture
- Docker components (daemon, CLI, registry)

### Why Docker?
- Consistency across environments
- Isolation of applications
- Resource efficiency
- Quick deployment
- Version control and component reuse
- Microservices architecture support

## Installation & Setup
### System Requirements
- Windows requirements
- Linux requirements
- macOS requirements

### Installation Steps
1. Download Docker Desktop/Docker Engine
2. Install Docker
3. Verify installation (`docker --version`)
4. Configure Docker settings
5. Test installation (`docker run hello-world`)

## Docker Fundamentals
### Basic Commands
```bash
# Version check
docker --version

# Docker info
docker info

# Download image
docker pull [image-name]

# List images
docker images

# List containers
docker ps
docker ps -a

# Run container
docker run [options] [image-name]

# Stop container
docker stop [container-id/name]

# Remove container
docker rm [container-id/name]

# Remove image
docker rmi [image-id/name]
```

## Working with Containers
### Container Lifecycle
1. Create container
2. Start container
3. Stop container
4. Restart container
5. Remove container

### Container Operations
```bash
# Run container in detached mode
docker run -d [image-name]

# Run container with port mapping
docker run -p [host-port]:[container-port] [image-name]

# Run container with name
docker run --name [container-name] [image-name]

# Execute command in running container
docker exec -it [container-id/name] [command]

# Container logs
docker logs [container-id/name]

# Container stats
docker stats [container-id/name]
```

## Docker Images
### Working with Images
- Pulling images
- Listing images
- Removing images
- Image layers
- Image history
- Image tagging
- Pushing to registry

### Docker Hub
- Public repositories
- Private repositories
- Image tags
- Official images
- Automated builds

## Dockerfile
### Basic Structure
```dockerfile
# Base image
FROM [base-image]

# Set working directory
WORKDIR /app

# Copy files
COPY . .

# Run commands
RUN [command]

# Set environment variables
ENV KEY=value

# Expose ports
EXPOSE [port]

# Define entry point
ENTRYPOINT ["executable"]

# Define default commands
CMD ["executable","param1","param2"]
```

### Building Images
```bash
# Build image
docker build -t [image-name] .

# Build with specific Dockerfile
docker build -f [dockerfile] -t [image-name] .
```

## Docker Compose
### Basic Structure
```yaml
version: '3'
services:
  web:
    build: .
    ports:
      - "5000:5000"
  redis:
    image: "redis:alpine"
```

### Common Commands
```bash
# Start services
docker-compose up

# Start in detached mode
docker-compose up -d

# Stop services
docker-compose down

# View logs
docker-compose logs

# List services
docker-compose ps
```

## Docker Networking
### Network Types
- Bridge
- Host
- None
- Overlay
- Macvlan

### Network Commands
```bash
# List networks
docker network ls

# Create network
docker network create [network-name]

# Connect container to network
docker network connect [network] [container]

# Inspect network
docker network inspect [network]
```

## Docker Volumes
### Volume Types
- Named volumes
- Bind mounts
- tmpfs mounts

### Volume Commands
```bash
# Create volume
docker volume create [volume-name]

# List volumes
docker volume ls

# Inspect volume
docker volume inspect [volume-name]

# Remove volume
docker volume rm [volume-name]
```

## Docker Security
### Best Practices
1. Use official base images
2. Scan images for vulnerabilities
3. Implement least privilege principle
4. Use secrets management
5. Regular security updates
6. Resource limitations
7. Network segmentation

### Security Commands
```bash
# Run security scan
docker scan [image-name]

# View security options
docker info --format '{{.SecurityOptions}}'
```

## Docker in Production
### Considerations
1. Container orchestration (Kubernetes/Swarm)
2. Monitoring and logging
3. CI/CD integration
4. High availability
5. Scaling strategies
6. Backup and disaster recovery
7. Performance optimization

## Best Practices
1. Use multi-stage builds
2. Optimize layer caching
3. Minimize image size
4. Use .dockerignore
5. Implement health checks
6. Tag images properly
7. Use docker-compose for development
8. Implement logging strategy
9. Regular cleanup
10. Documentation

## Practical Exercises
1. Build a simple web application
2. Create multi-container application
3. Implement CI/CD pipeline
4. Set up monitoring
5. Deploy to production

## Resources
- [Official Docker Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Docker GitHub](https://github.com/docker)
- [Docker Community Forums](https://forums.docker.com/)

## Troubleshooting
Common issues and solutions:
1. Container won't start
2. Network connectivity issues
3. Volume mount problems
4. Resource constraints
5. Image build failures

Remember: Practice is key! Start with basic concepts and gradually move to advanced topics. Build real-world projects to gain hands-on experience.
