# 🌩️ AWS and Azure DevOps Interview Questions

## Azure Section
---

### **1. What is Azure Data Factory and how do we use it?**
Azure Data Factory (ADF) is a cloud-based ETL/ELT service used to move and transform data.

We use it by creating:  
🔗 **Linked Services** – connections to data sources  
📂 **Datasets** – structure of input/output data  
🛠️ **Pipelines** – workflows of activities  
⏱️ **Triggers** – scheduling or event-based execution  

---

### **2. How do we deploy a .NET application?**
✔️ Build the .NET application  
✔️ Publish output (ZIP, DLLs, or Docker image)  

Deploy to:  
🌐 Azure App Service  
🐳 AKS (Azure Kubernetes Service) using Docker + ACR  
🖥️ IIS on Windows Server  

Deployment methods: Azure DevOps, Visual Studio Publish, Azure CLI.

---

### **3. What is the architecture of Azure AKS?**
Azure AKS is a managed Kubernetes service where:

🧠 **Control Plane** – managed by Azure (API server, scheduler, etcd)  
🖥️ **Node Pools** – worker nodes running containers  
🌐 **Networking** – Azure CNI, Load Balancer, Ingress  
💾 **Storage** – Azure Disk, Azure Files  

Workloads deployed using pods, deployments, services, ingress controllers.

---

### **4. Difference between Azure Blob Storage and Azure Files**
📦 **Azure Blob Storage** – object storage for unstructured data (images, logs, backups).  
📁 **Azure Files** – SMB/NFS shared file system, mountable like a network share.  

- Blob = object storage  
- Files = file system storage  

---

### **5. Explain Azure DevOps pipeline end-to-end**
1. 👨‍💻 Developer commits code  
2. 🔧 CI pipeline builds, tests, generates artifacts  
3. 🚀 CD pipeline deploys to Dev → QA → Prod  
4. 🔐 Uses service connections, variables, secrets  
5. 📊 Includes approvals, monitoring, rollback  

---

### **6. Explain Azure CI using YAML**
YAML pipeline defines the CI as code:

📌 `trigger:` – when pipeline runs  
⚙️ `steps:` – restore, build, test, publish  
🖥️ Runs on Microsoft-hosted agents  
📦 Produces build artifacts  

---

### **7. How to deploy a multi-stage pipeline using YAML in Azure DevOps**
A single YAML file includes multiple stages:

🏗️ **Build Stage** – compile and create artifacts  
🧪 **Dev/QA Stage** – deployment for testing  
🚀 **Prod Stage** – production release  
🔄 Artifacts flow between stages  
🛑 Approvals/gates can be applied before Prod  

---

# ☁️ AWS Section
---

## **AWS Questions List**
1. ECS Architecture  
2. EKS Architecture  
3. End-to-end project pipeline  
4. Difference between AWS and Azure  
5. Difference between MySQL and PostgreSQL  
6. GitHub Actions pipeline  
7. Challenges in Terraform automation  
8. How to deploy a Docker application  
9. Docker vs VM  
10. MySQL port number  
11. How to secure a Docker image  

---

### **1. ECS Architecture**
ECS is AWS’s container orchestration service.

🧠 Control Plane → ECS Service + Cluster Manager  
🖥️ Worker Layer → EC2 instances or Fargate tasks  
📦 Tasks → Task Definitions running containers  
🌐 Networking → ALB/NLB + Security Groups  
⚙️ Autoscaling → container + service autoscaling  

---

### **2. EKS Architecture**
AWS managed Kubernetes service:

🧠 Control Plane → API server, etcd, scheduler  
🖥️ Worker Nodes → EC2 or Fargate  
🌐 Networking → VPC CNI, Ingress Controller, ALB  
💾 Storage → EBS, EFS  
⚙️ Runs Kubernetes workloads (deployments, pods, services)  

---

### **3. End-to-End Project Pipeline**
4. 👨‍💻 Developer writes code  
5. 🔁 Pushes to Git  
6. 🔧 CI pipeline → build, test, create artifact/image  
7. 🐳 Image pushed to registry (ECR/ACR/DockerHub)  
8. 🚀 CD pipeline → deploy to ECS/EKS/VMs  
9. 🔍 Monitoring (CloudWatch, Prometheus, Grafana)  
10. 📦 Versioning, rollback, approvals  

---

### **4. Difference Between AWS and Azure**
☁️ **AWS**
- Largest cloud provider  
- Strong compute, container orchestration  
- Complex pricing  

☁️ **Azure**
- Strong Microsoft ecosystem support  
- Hybrid cloud leader  
- Easy CI/CD with Azure DevOps  

---

### **5. Difference Between MySQL and PostgreSQL**
🐬 **MySQL**
- Simple, fast  
- Limited advanced features  
- Great for web apps  

🐘 **PostgreSQL**
- Advanced, powerful SQL engine  
- Strong ACID compliance  
- JSONB, extensions, analytics features  

---

### **6. GitHub Actions Pipeline**
GitHub’s built-in CI/CD system.

⚙️ Workflows in `.github/workflows/*.yml`  
🔁 Triggered on push, PR, schedule  
🧩 Jobs run in sequence/parallel  
🖥️ Hosted or self-hosted runners  
🚀 Deploy to AWS/GCP/Azure via marketplace actions  

---

### **7. Terraform Automation Challenges**
⚠️ State file conflicts  
⚠️ Backend misconfigurations  
⚠️ Module versioning issues  
⚠️ Drift between infra and Terraform state  
⚠️ Sensitive variable handling  
⚠️ Slow plan/apply for large infra  
⚠️ Locking issues on team environments  

---

### **8. How to Deploy a Docker Application**
1. 🐳 Create Dockerfile  
2. 🔧 Build image: `docker build -t app .`  
3. 📦 Run container: `docker run -p 8080:80 app`  
4. 🚀 Push to registry  
5. 🌐 Deploy to ECS/EKS/Kubernetes/VM  

---

### **9. Docker vs VM**
🐳 **Docker**
- Lightweight, fast  
- Shares OS kernel  
- Ideal for microservices  

🖥️ **VM**
- Heavy, full OS  
- Strong isolation  
- Suitable for legacy/monolithic apps  

---

### **10. MySQL Port Number**
🔌 **Default port: 3306**

---

### **11. How to Secure Docker Image**
🔒 Use minimal base images  
🔒 Scan with Trivy/Clair  
🔒 Avoid secrets in images  
🔒 Use multi-stage builds  
🔒 Run as non-root  
🔒 Apply patches  
🔒 Sign images using Docker Content Trust  

---

## 🔔 Follow for More DevOps Interview Questions  
📺 **YouTube Channel:** DevOps With Namdev  
👉 https://www.youtube.com/@namdev.devops
