## 1. docker pull `<image-name>`  
The command is used to download (pull) a Docker image from a remote registry — usually Docker Hub — onto your local machine.

🔍 Explanation:

- docker pull → fetches the image layers from the registry.

- <image-name> → the name of the image you want to download (e.g., ubuntu, nginx, mysql).

## 2. docker images
docker images is a Docker command used to list all the images available on your local system.

What it shows:

- REPOSITORY – Name of the image (e.g., ubuntu, nginx)

- TAG – Version (e.g., latest)

- IMAGE ID – Unique image identifier

- CREATED – When it was created

- SIZE – Size of the image

## 3. docker run -it `<image-name>`
To run a Docker container interactively.

Here’s what each part means:

- docker run → starts a new container from a Docker image.

- -i → keeps STDIN (input) open even if not attached (interactive mode).

- -t → allocates a pseudo-TTY (terminal), so you get an interactive shell.

- `<image-name>` → the name (or ID) of the Docker image you want to run.

## 4. docker start `<container-name or id>`
Used to start an existing (stopped) container.

## 5. docker stop `<container-name>`
Used to gracefully stop a running container.

## 6. docker ps
To list all running Docker containers.

## 7. docker ps -a
To list all containers — both running and stopped ones.

## 8. docker rmi `<image-name>`
To remove (delete) a Docker image from your local system.

- docker rmi → stands for remove image.

- <image-name> or <image-id> → the image you want to delete.

## 9. docker rm `<container-name>`
To remove (delete) a container from your system.

## 10. docker pull `<image-name>:<version>`
To download a specific version (tag) of a Docker image from a registry — usually Docker Hub — to your local machine.

- docker pull → fetches an image from a registry (like Docker Hub).

- `<image-name>` → the name of the image (e.g., ubuntu, nginx, mysql).

- `:<version>` → the tag that specifies which version you want.

🧠 Examples:

docker pull mysql:8.0

## 11. docker run -d -e MYSQL_ROOT_PASSWORD=`<Add_password>` `<image-name>`
To run a Docker container in detached mode (-d), set an environment variable (-e), and use an image to create the container.

- docker run → start a new container.

- -d → detached mode (runs in the background).

- -e → set an environment variable inside the container.

- MYSQL_ROOT_PASSWORD=<Add_Password> → sets the MySQL root password.

- `<image-name>` → the Docker image to run (e.g., mysql).

## 12. docker run -d -e MYSQL_ROOT_PASSWORD=`<Add_password>` `<image-name>`:`<version>`
To run a Docker container of specific version in detached mode (-d), set an environment variable (-e), and use an image to create the container.

## **PORT BINDING**
## 13. docker run -d -p `<host-port>`:`<container-port>` `<image-name>`
This is the generic format for port mapping when running a Docker container.

| Part               | Meaning                                      |
| ------------------ | -------------------------------------------- |
| `docker run`       | Creates & runs a new container               |
| `-d`               | Detached mode (runs in background)           |
| `-p`               | Port mapping (expose container port to host) |
| `<host-port>`      | Port on your **machine** (laptop/server)     |
| `<container-port>` | Port inside the **container**                |
| `<image-name>`     | Docker image to create container from        |

**Example: Running MySQL**

docker run -d -p 8080:3306 -e MYSQL_ROOT_PASSWORD=pass123 mysql

## **Troubleshoot Command**
## 14. docker logs `<container_ID/Name>`
To view the logs (output) from a container

## 15. docker exec -it `<container_id>` /bin/bash
Open an interactive bash shell inside a running container.

## 16. docker exec -it `<container_id>` /bin/sh
Open an interactive sh shell inside a running container.

When to use this:

- Some minimal images (like Alpine, BusyBox, or scratch) don’t include bash, so /bin/bash will fail.

- In those cases, use /bin/sh.



