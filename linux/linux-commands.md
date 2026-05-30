# Linux Commands for DevOps

## Docker Commands

### docker ps

```bash
docker ps
```

Explanation:
Displays all currently running Docker containers.

Purpose:
Used to monitor active containers running on the server.

---

### docker images

```bash
docker images
```

Explanation:
Lists all Docker images available on the system.

Purpose:
Used to verify downloaded or custom-built images.

---

### docker build -t myapp .

```bash
docker build -t myapp .
```

Explanation:
Builds a Docker image from the Dockerfile in the current directory.

Purpose:
Used to containerize applications for deployment.

---

### docker run -d -p 80:80 myapp

```bash
docker run -d -p 80:80 myapp
```

Explanation:
Runs a Docker container in detached mode and maps port 80.

Purpose:
Used to deploy and expose applications through Docker containers.

---

# Kubernetes Commands

## kubectl get pods

```bash
kubectl get pods
```

Explanation:
Displays all running pods in the Kubernetes cluster.

Purpose:
Used to monitor application containers in Kubernetes.

---

## kubectl get nodes

```bash
kubectl get nodes
```

Explanation:
Shows all worker and master nodes in the Kubernetes cluster.

Purpose:
Used to verify cluster health and node availability.

---

## kubectl apply -f deployment.yml

```bash
kubectl apply -f deployment.yml
```

Explanation:
Applies Kubernetes configuration from a YAML file.

Purpose:
Used to deploy applications and services in Kubernetes.

---

# Jenkins Commands

## systemctl start jenkins

```bash
systemctl start jenkins
```

Explanation:
Starts the Jenkins service.

Purpose:
Used to run Jenkins CI/CD server.

---

## systemctl status jenkins

```bash
systemctl status jenkins
```

Explanation:
Checks the current status of Jenkins service.

Purpose:
Used to verify whether Jenkins is running successfully.

---

# Linux Commands

## top

```bash
top
```

Explanation:
Displays real-time running processes, CPU usage, memory usage, and system performance.

Purpose:
Used for server monitoring and troubleshooting high resource usage.

---

## free -m

```bash
free -m
```

Explanation:
Shows RAM and swap memory usage in MB.

Purpose:
Used to monitor memory utilization on Linux servers.

---

## df -h

```bash
df -h
```

Explanation:
Displays disk space usage in human-readable format.

Purpose:
Used to monitor storage availability and filesystem usage.

---

## netstat -tulnp

```bash
netstat -tulnp
```

Explanation:
Displays active ports, network connections, and listening services.

Purpose:
Used to troubleshoot networking issues and verify application ports.
