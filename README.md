# DevOps Docker & Kubernetes Lab

A hands-on lab showcasing Docker image building, Kubernetes deployments, and container orchestration.  
This repository is designed as a complete *end-to-end DevOps practice environment* and is part of my Azure DevOps/DevOps portfolio.

---

## 📌 Tech Stack
- Docker
- Kubernetes (k8s)
- Helm 
- Git & GitHub
- VS Code
- Minikube / Kind / AKS (any can be used)

---

## 🔥 Features Covered
✔ Build custom Nginx Docker image  
✔ Build Node.js app Docker image  
✔ Deploy both apps on Kubernetes  
✔ Expose apps using NodePort services  
✔ Ingress routing demo  
✔ Clean folder structure for real-world DevOps projects  

---

## 📁 Folder Structure

```
devops-docker-k8s-lab/
 ├─ docker/
 │   ├─ Dockerfile.nginx
 │   ├─ Dockerfile.node
 │   ├─ index.html
 │   ├─ server.js
 │   └─ package.json
 ├─ k8s-manifest-files/
 │   ├─ nginx-deployment.yaml
 │   ├─ nginx-service.yaml
 │   ├─ node-deployment.yaml
 │   ├─ node-service.yaml
 │   └─ ingress.yaml
 └─ README.md
```

---

## 🐳 Docker Commands

### 👉 Build Nginx Image
```sh
docker build -t custom-nginx -f docker/Dockerfile.nginx ./docker
```

### 👉 Build Node App Image
```sh
docker build -t custom-node -f docker/Dockerfile.node ./docker
```

### 👉 Run Nginx Container
```sh
docker run -p 8080:80 custom-nginx
```

### 👉 Run Node App Container
```sh
docker run -p 3000:3000 custom-node
```

---

## ☸️ Kubernetes Deployment

### 👉 Deploy Nginx
```sh
kubectl apply -f k8s-manifest-files/nginx-deployment.yaml
kubectl apply -f k8s-manifest-files/nginx-service.yaml
```

### 👉 Deploy Node App
```sh
kubectl apply -f k8s-manifest-files/node-deployment.yaml
kubectl apply -f k8s-manifest-files/node-service.yaml
```

### 👉 Deploy Ingress (Optional)
```sh
kubectl apply -f k8s-manifest-files/ingress.yaml
```

---

## 🔍 Verification

### Check Deployments
```sh
kubectl get deployments
```

### Check Pods
```sh
kubectl get pods
```

### Check Services
```sh
kubectl get svc
```

### Access Apps
```
http://localhost:30080/nginx
http://localhost:30001/node
```

(Or via ingress host if configured)

---

### Commands to install the helm chart
``` sh
helm install myapp ./helm-chart/myapp
```

## update

``` sh
helm upgrade myapp ./helm-chart/myapp
```
## uninstall
``` sh
helm uninstall myapp
```

----

## 🎯 Purpose of This Lab
This repo demonstrates my practical experience across:
- Containerization  
- Kubernetes deployments  
- YAML writing  
- Local cluster testing  
- Git repository organization  
- Infrastructure-as-Code mindset  

This is part of my bigger Azure DevOps portfolio.

---

## 📬 Contact
If you want to collaborate or explore my DevOps work:  
**LinkedIn**: *Add later*  
**GitHub Projects**: *More labs coming soon* 🚀
