For DevOps Engineers, Docker is one of the important technologies you must learn.

Docker is a platform that allows developers to create, deploy, and run applications inside containers.

A container is a lightweight, stand-alone, executable software package that includes everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings.

Containers are isolated from each other and the host system.

Why is Docker Important for DevOps?

1. Consistency:
containers package up all dependencies, an application will run the same regardless of where the container is run.

This eliminates the "it works on my machine" problem.
  
2. Isolation:
Containers ensure that applications run in isolation from each other.

This means if one application crashes, it won't affect others.

3. Scalability:
With Docker, it's easy to scale applications up or down, depending on the demand, by simply starting or stopping containers.

4. Portability:
You can build a container on your local machine, then deploy it to various environments (e.g., QA, staging, production) without changes.

5. Infrastructure Efficiency:
Containers are lightweight compared to virtual machines, as they share the host system's OS, rather than needing their own operating system.

Fundamental Concepts:

1. Images:
Docker uses images to create containers. An image is a lightweight, stand-alone, executable package that includes everything needed to run a piece of software.

2. Containers:
A container is a runtime instance of an image. It's the "live" version of the Docker image.

3. Dockerfile:
A script with commands to build a Docker image. It defines how the image should be built, what software it should contain, and how it should run.

4. Docker Hub:
A cloud-based registry where Docker users and partners create, test, store, and distribute container images.

5. Docker Compose:
A tool for defining and running multi-container Docker applications.

With Compose, you use a YAML file to define the services, networks, and volumes, and then start all services with a single command.

6. Volumes:
Used to store data outside of containers, ensuring that data persists even if the container is deleted.

How Does Docker Work?

At a high level, Docker works by using a technology called containerization.

Unlike traditional virtualization, where each application requires a separate operating system instance, containerization allows multiple containers to run on a single OS instance.

The Docker engine, which is responsible for building and running containers, achieves this.

Docker vs. Traditional VMs:

Performance: Containers are lightweight and share the host OS, while VMs have their own full OS instance.
  
Size: VM images are often several GBs because they include a full OS. Docker images are much smaller as they only include the application and its dependencies.

Startup Time: Containers can start almost instantly, whereas VMs can take several minutes.


docker pull image-name
docker run --name cont-app1 -p 80:8080 -d image-name
docker ps
docker ps -a
docker ps -a -q
docker exec -it <container-name> /bin/sh    #Connect to Container Terminal
docker stop <container-name>
docker start  <container-name>
docker stop <container-name> 
docker rm <container-name>
docker images
docker rmi  <image-id>
---
     Commands                               |    Description                                  |
| -------------------------------           | --------------------------------------------- |
| docker ps                                 | List all running containers |
| docker ps -a                    	    | List all containers stopped, running |
| docker stop container-id                  | Stop the container which is running |
| docker start container-id     	    | Start the container which is stopped |
| docker restart container-id    	    | Restart the container which is running |
| docker port container-id       	    | List port mappings of a specific container |
| docker rm container-id or name 	    | Remove the stopped container |
| docker rm -f container-id or name	    | Remove the running container forcefully |
| docker pull image-info         	    | Pull the image from docker hub repository |
| docker pull helloworld        	    | Pull the image from docker hub repository |
| docker exec -it container-name /bin/sh    | Connect to linux container and execute commands in container |
| docker rmi image-id            	    | Remove the docker image |
| docker logout                  	    | Logout from docker hub |
| docker login -u username -p password 	    | Login to docker hub |
| docker stats                    	    | Display a live stream of container(s) resource usage statistics |
| docker top container-id or name 	    | Display the running processes of a container |
| docker version                 	    | Show the Docker version information |

------------------------------------------------------------------------------------------


Docker is a powerful containerization platform, and here are some commonly used Docker commands:

1. **Building Images:**
   - `docker build -t image_name:tag .`: Build a Docker image from the current directory.

2. **Running Containers:**
   - `docker run image_name:tag`: Create and start a container based on the specified image.
   - `docker run -d image_name:tag`: Run a container in detached mode (in the background).
   - `docker exec -it container_id command`: Run a command inside a running container.

3. **Listing and Managing Containers:**
   - `docker ps`: List running containers.
   - `docker ps -a`: List all containers (including stopped ones).
   - `docker stop container_id`: Stop a running container.
   - `docker rm container_id`: Remove a stopped container.
   - `docker rm -f container_id`: Forcefully remove a running container.

4. **Images:**
   - `docker images`: List available images on your machine.
   - `docker rmi image_id`: Remove a Docker image.
   - `docker pull image_name:tag`: Pull an image from a Docker registry.

5. **Networking:**
   - `docker network ls`: List Docker networks.
   - `docker network inspect network_name`: Inspect details of a network.
   - `docker network create network_name`: Create a Docker network.

6. **Volumes:**
   - `docker volume ls`: List Docker volumes.
   - `docker volume create volume_name`: Create a Docker volume.
   - `docker volume inspect volume_name`: Inspect details of a volume.

7. **Logs and Inspecting:**
   - `docker logs container_id`: View logs of a running container.
   - `docker inspect container_id`: View detailed information about a container.
   - `docker inspect image_id`: View detailed information about an image.

8. **Clean-Up:**
   - `docker system df`: Show Docker disk usage.
   - `docker system prune`: Remove all stopped containers, unused networks, and dangling images.
   - `docker system prune -a`: Remove all stopped containers, networks, and images (including unused ones).

9. **Compose (for multi-container applications):**
   - `docker-compose up`: Start services defined in a `docker-compose.yml` file.
   - `docker-compose down`: Stop and remove containers, networks, and volumes defined in a `docker-compose.yml` file.

Remember to replace `image_name`, `container_id`, `image_id`, etc., with the actual names or IDs in your setup. Additionally, Docker has many more commands and options. You can explore the [official Docker documentation](https://docs.docker.com/) for more in-depth information and usage examples.
