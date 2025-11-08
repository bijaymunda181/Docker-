## 1. what is Docker

Docker is a platform used to build, run, and manage applications inside containers.

✅ Simple Definition:

Docker allows you to package an application along with everything it needs (code, libraries, dependencies) into a container so that it can run the same way on any system.

## 2. What is Container

A container is a lightweight, isolated environment where an application runs along with all its required files, libraries, and dependencies.

✅ Simple definition:

A container packages an application and everything it needs so that it runs the same way on any system.

Example:

If you run an app on your laptop and then move it to a server, the app may not work because the server may not have the correct version of Python/Java or required packages.

But if you run the app inside a container, it doesn’t matter what is installed on the server — the container already has everything inside it.

🚚 Analogy:

Think of a container like a sealed lunch box 🥡:

- Whatever food (application + dependencies) you put inside stays the same.

- You can carry and open it anywhere, and it will taste the same.

| Feature                                    | Container |
| ------------------------------------------ | --------- |
| Runs applications in isolated environments | ✅         |
| Lightweight and fast                       | ✅         |
| Uses fewer resources than VMs              | ✅         |
| Works the same on any system               | ✅         |

## 3. What is a Docker Image?
A Docker image is a read-only template used to create containers.

docker pull nginx

## 4. How to build a Docker container?

Steps:

1. Create a Dockerfile

2. Build the image

docker build -t myimage .

3. Run the container

docker run -d --name mycontainer myimage

## 5. How to check container logs in Docker?
docker logs container-name

## ✅ **KUBERNETES BASICS**
## 6. What is Kubernetes?
Kubernetes (K8s) is an orchestration tool used to manage containers at scale (deploy, manage, scale, update).

## 7. What is Docker and Kubernetes - EKS?

- Docker: Used to build and run containers.

- Kubernetes: Used to manage many containers.

- EKS: Amazon Elastic Kubernetes Service: Kubernetes managed by AWS.

## 8. What are the components available in Kubernetes?

Two types of components:

**Control Plane (Master Node)**

- API server

- etcd

- Scheduler

- Controller Manager

**Worker Node**

- Kubelet

- Kube-proxy

- Container runtime (Docker / containerd)

## 9. What is Master Plane and Data Plane?

- Master plane (control plane): Decides what happens (brain).

- Data plane (worker nodes): Executes workloads (muscles).


