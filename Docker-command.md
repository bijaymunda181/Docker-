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
