
---

# **Working with Docker Containers**

## **Introduction to Docker Containers**
Docker containers are **lightweight, portable, and executable units** that encapsulate an application and all its dependencies. In the previous step, we briefly worked with Docker containers. In this module, we’ll dive deeper into the fundamentals of using Docker containers—from launching and running them to managing their lifecycle.

---

## **Running Containers**

To run a container, use the `docker run` command followed by the name of the image.

For example, to run a container using the **official Ubuntu image** pulled from Docker Hub:

```bash
docker run ubuntu
```

> This command launches a container based on the Ubuntu image. If the image isn't available locally, Docker will automatically pull it from Docker Hub.

However, this container may exit immediately if no command is specified. To start it again:

```bash
docker start CONTAINER_ID
```

You can view all containers (including stopped ones) using:

```bash
docker ps -a
```

---

## **Launching Containers with Custom Options**

Docker offers various options for customizing container behavior, such as:

### **1. Setting Environment Variables**

```bash
docker run -e "MY_VARIABLE=my-value" ubuntu
```

### **2. Running Containers in the Background**

To run a container in **detached mode** (in the background):

```bash
docker run -d ubuntu
```

> The `-d` flag stands for “detached.” This lets you continue using the terminal while the container runs in the background.

---

## **Container Lifecycle**

Each Docker container has a lifecycle that includes **creation, running, stopping, restarting, and removal**.

### **Starting a Container**

```bash
docker start container_name_or_id
```

### **Stopping a Container**

```bash
docker stop container_name_or_id
```

### **Restarting a Container**

```bash
docker restart container_name_or_id
```

---

## **Removing Containers**

To delete a container:

```bash
docker rm container_name_or_id
```

> Note: Removing a container does not delete the image. You can reuse the image to create new containers.

---

## **Side Hustle Task: Docker Container Operations**

Perform the following steps as part of your hands-on practice:

### **1. Start a Container and Run a Simple Command**

- Pull the Ubuntu image (if not already available):

```bash
docker pull ubuntu
```

- Run a simple command within a container:

```bash
docker run ubuntu uname -a
```

### **2. Stop the Container and Verify Its Status**

- Stop a running container:

```bash
docker stop container_name_or_id
```

- Verify the container's status:

```bash
docker ps -a
```

> Look under the **STATUS** column to confirm whether the container is running, stopped, or exited.

### **3. Restart the Container and Observe Changes**

- Restart a stopped container:

```bash
docker restart container_name_or_id
```

- Re-check the container’s status:

```bash
docker ps -a
```

### **4. Remove the Container**

- Stop the container (if running):

```bash
docker stop container_name_or_id
```

- Remove the container:

```bash
docker rm container_name_or_id
```

- Verify that it has been removed:

```bash
docker ps -a
```

> The container should no longer appear in the list.

---

## ✅ Summary

You’ve learned the following key Docker container concepts:

- How to **run**, **customize**, and **detach** containers
- How to **start**, **stop**, and **restart** containers
- How to **remove** containers and confirm their lifecycle status

Mastering these container operations is essential for efficient Docker-based development and deployment.

---
