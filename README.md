# 🚀 DevOps Portfolio - Suryamoorthy

Hi, I'm Suryamoorthy, an AWS & DevOps Engineer fresher passionate about cloud infrastructure, automation, CI/CD pipelines, and container orchestration.

---

# 🔧 Skills

* AWS
* Docker
* Kubernetes
* Jenkins
* Linux
* Git & GitHub
* Terraform
* Ansible
* Prometheus
* Grafana
* YAML

---

# 📁 Projects

## Docker Multi-Container Project

### Dockerfile

```dockerfile
FROM nginx:latest
COPY . /usr/share/nginx/html
EXPOSE 80
```

### docker-compose.yml

```yaml
version: '3'

services:
  web:
    build: .
    ports:
      - "80:80"
```

Purpose:
Containerized applications using Docker and Docker Compose.

---

# ☸️ Kubernetes Project

### deployment.yml

```yaml
apiVersion: apps/v1
kind: Deployment

metadata:
  name: nginx-deployment

spec:
  replicas: 2

  selector:
    matchLabels:
      app: nginx

  template:
    metadata:
      labels:
        app: nginx

    spec:
      containers:
      - name: nginx
        image: nginx:latest

        ports:
        - containerPort: 80
```

### service.yml

```yaml
apiVersion: v1
kind: Service

metadata:
  name: nginx-service

spec:
  selector:
    app: nginx

  ports:
    - protocol: TCP
      port: 80
      targetPort: 80

  type: LoadBalancer
```

Purpose:
Managed application deployment and services in Kubernetes cluster.

---

# 🔄 Jenkins CI/CD Pipeline

### Jenkinsfile

```groovy
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Ayrus-kira/devops-portfolio.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-portfolio ./docker-project'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 devops-portfolio'
            }
        }
    }
}
```

Purpose:
Automated CI/CD pipeline using Jenkins and Docker.

---

# 📊 Monitoring Stack

### prometheus.yml

```yaml
global:
  scrape_interval: 15s

scrape_configs:
  - job_name: 'prometheus'

    static_configs:
      - targets: ['localhost:9090']
```

Purpose:
Configured monitoring and metrics collection using Prometheus.

---

# ☁️ Terraform Infrastructure

### main.tf

```terraform
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "web" {
  ami           = "ami-0c02fb55956c7d316"
  instance_type = "t2.micro"

  tags = {
    Name = "DevOpsServer"
  }
}
```

Purpose:
Provisioned AWS infrastructure using Terraform.

---

# ⚙️ Ansible Automation

### install-nginx.yml

```yaml
---
- name: Install NGINX on servers
  hosts: all
  become: yes

  tasks:

    - name: Install nginx
      apt:
        name: nginx
        state: present
        update_cache: yes

    - name: Start nginx service
      service:
        name: nginx
        state: started
        enabled: yes
```

Purpose:
Automated server configuration and software installation using Ansible.

---

# 🐧 Linux Commands for DevOps

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
Used to monitor server memory utilization.

---

## df -h

```bash
df -h
```

Explanation:
Displays disk space usage in human-readable format.

Purpose:
Used to monitor storage availability.

---

## netstat -tulnp

```bash
netstat -tulnp
```

Explanation:
Displays open ports and active network connections.

Purpose:
Used to troubleshoot networking and services.

---

# 🐳 Docker Commands

## docker ps

```bash
docker ps
```

Explanation:
Displays running Docker containers.

Purpose:
Used to monitor active containers.

---

## docker images

```bash
docker images
```

Explanation:
Lists Docker images available on the system.

Purpose:
Used to verify container images.

---

## docker build -t myapp .

```bash
docker build -t myapp .
```

Explanation:
Builds Docker image from Dockerfile.

Purpose:
Used to containerize applications.

---

## docker run -d -p 80:80 myapp

```bash
docker run -d -p 80:80 myapp
```

Explanation:
Runs Docker container in detached mode.

Purpose:
Used to deploy applications inside containers.

---

# ☸️ Kubernetes Commands

## kubectl get pods

```bash
kubectl get pods
```

Explanation:
Displays running pods in Kubernetes cluster.

Purpose:
Used to monitor application containers.

---

## kubectl get nodes

```bash
kubectl get nodes
```

Explanation:
Displays Kubernetes cluster nodes.

Purpose:
Used to verify cluster health.

---

## kubectl apply -f deployment.yml

```bash
kubectl apply -f deployment.yml
```

Explanation:
Applies Kubernetes configuration file.

Purpose:
Used to deploy applications to Kubernetes cluster.

---

# ☁️ AWS Commands

## aws configure

```bash
aws configure
```

Explanation:
Configures AWS CLI credentials.

Purpose:
Used to connect Linux server with AWS account.

---

## aws s3 ls

```bash
aws s3 ls
```

Explanation:
Lists available S3 buckets.

Purpose:
Used to manage cloud storage.

---

## aws ec2 describe-instances

```bash
aws ec2 describe-instances
```

Explanation:
Displays EC2 instance details.

Purpose:
Used to monitor AWS virtual machines.

---

# 🔀 Git & GitHub Commands

## git init

```bash
git init
```

Explanation:
Initializes Git repository.

Purpose:
Used to start version control.

---

## git status

```bash
git status
```

Explanation:
Displays repository status.

Purpose:
Used to verify changed files.

---

## git add .

```bash
git add .
```

Explanation:
Adds files to staging area.

Purpose:
Used before committing changes.

---

## git commit -m "message"

```bash
git commit -m "Initial commit"
```

Explanation:
Creates project snapshot.

Purpose:
Used to track project history.

---

## git push

```bash
git push
```

Explanation:
Uploads code to GitHub.

Purpose:
Used to share and backup projects.

---

# 📸 Screenshots

* Jenkins Pipeline Success
* Kubernetes Pods Running
* Docker Containers Running
* AWS EC2 Dashboard
* Grafana Monitoring Dashboard

---

# 🌐 GitHub

GitHub: https://github.com/Ayrus-kira
