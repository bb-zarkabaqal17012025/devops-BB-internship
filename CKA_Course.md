# Kubernetes Concepts Summary  

## 🌍 Introduction to Kubernetes  

Kubernetes (often abbreviated as **K8s**) is an open-source **container orchestration platform** designed to automate the deployment, scaling, and management of containerized applications. It enables developers to manage workloads efficiently by abstracting the complexities of infrastructure and providing a unified interface for running applications at scale. Kubernetes ensures high availability, fault tolerance, and optimal resource utilization across multiple nodes in a cluster. With features like **self-healing, load balancing, service discovery, and automated rollouts**, Kubernetes has become the industry standard for running microservices and cloud-native applications.

---

## 1. Kubernetes Control Plane Components  

The **control plane** manages the overall cluster state and ensures that workloads run as expected. Key components include:

### 🛠 Kube-API Server  
- The central management entity of Kubernetes.  
- Exposes REST APIs for interacting with the cluster.  
- Handles authentication, authorization, and request validation.  
- Acts as the communication hub between other control plane components.

### 🏗 Kube-Controller Manager  
- Runs multiple controllers in a single process:  
  - **Node Controller**: Monitors node health and marks them as unavailable if they become unresponsive.  
  - **Replication Controller**: Ensures the desired number of pods are running.  
  - **Service Account & Token Controller**: Manages authentication tokens.  
- Continuously monitors the cluster state and reconciles it with the desired state.

### 📅 Kube-Scheduler  
- Assigns new pods to worker nodes based on:  
  - Resource availability (CPU, memory, etc.).  
  - Node affinity and anti-affinity rules.  
  - Taints and tolerations.  
  - Pod priority and scheduling policies.  
- Ensures efficient resource utilization and workload distribution.

---

## 2. Kubernetes Node Components  

Worker nodes run application workloads and report to the control plane. Key components on nodes:

### 🔗 Kubelet  
- Runs on every worker node.  
- Ensures pods and their containers are running.  
- Communicates with the API server for updates.  
- Uses **container runtime** (like Docker, containerd) to manage containers.

### 🔀 Kube-Proxy  
- Handles networking for pods and services.  
- Maintains network rules to ensure seamless communication between services and external traffic.  
- Implements **iptables** or **IPVS** for forwarding traffic.

---

## 3. Workloads  

### 🏗 Pods  
- The **smallest deployable unit** in Kubernetes.  
- Contains one or more containers sharing **networking and storage**.  
- Has its own **IP address** and can communicate with other pods using this IP.  
- Managed by higher-level controllers like **ReplicaSets** and **Deployments**.

### 🔁 ReplicaSets  
- Ensures a specified number of pod replicas are always running.  
- If a pod fails, a new one is created automatically.  
- Example YAML definition:
  ```yaml
  apiVersion: apps/v1
  kind: ReplicaSet
  metadata:
    name: my-replicaset
  spec:
    replicas: 3
    selector:
      matchLabels:
        app: my-app
    template:
      metadata:
        labels:
          app: my-app
      spec:
        containers:
          - name: my-container
            image: nginx
🚀 Deployments
Provides declarative updates for applications.
Manages rolling updates and rollbacks.
Example Deployment command:
sh
Copy
Edit
kubectl create deployment my-app --image=nginx --replicas=3
Can be updated with:
sh
Copy
Edit
kubectl set image deployment/my-app nginx=nginx:latest
4. Services
Services allow communication between pods and external users. Key types:

🔵 ClusterIP (Default)
Exposes a service internally within the cluster.
Example:
yaml
Copy
Edit
apiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  selector:
    app: my-app
  ports:
    - protocol: TCP
      port: 80
      targetPort: 8080
🌍 NodePort
Exposes a service on a static port across all cluster nodes.
Accessible via NodeIP:NodePort.
Default range: 30000-32767.
Example:
yaml
Copy
Edit
apiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  type: NodePort
  selector:
    app: my-app
  ports:
    - protocol: TCP
      port: 80
      targetPort: 8080
      nodePort: 30001
☁ LoadBalancer
Exposes the service externally using a cloud provider’s load balancer.
Mostly used in managed Kubernetes clusters (AWS, GCP, Azure).
5. Namespaces
Used for logical separation of resources in a cluster.
Helps in organizing workloads and applying different policies.
Commonly used namespaces:
default – Default namespace for resources without a specified namespace.
kube-system – Contains Kubernetes control plane components.
kube-public – Readable by everyone (used for public configurations).
kube-node-lease – Maintains heartbeats for nodes.
Commands:

sh
Copy
Edit
kubectl get namespaces         # List all namespaces
kubectl create namespace dev   # Create a new namespace
kubectl delete namespace test  # Delete a namespace
6. Imperative vs Declarative Commands
🛠 Imperative Approach
Directly executes commands to manage Kubernetes resources.
Example:
sh
Copy
Edit
kubectl create deployment my-app --image=nginx --replicas=3
Quick and useful for testing but not recommended for production.
📜 Declarative Approach
Uses YAML/JSON configuration files to define the desired state.
Applied using kubectl apply -f <file.yaml>.
Recommended for production as it enables version control.
Example Deployment YAML:

yaml
Copy
Edit
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
        - name: my-container
          image: nginx
Apply it using:

sh
Copy
Edit
kubectl apply -f deployment.yaml
🔥 Conclusion
Kubernetes simplifies container orchestration by automating deployment, scaling, and management.
Control plane components manage the cluster, while worker nodes run workloads.
Pods, ReplicaSets, and Deployments ensure applications run reliably.
Services and Namespaces enable efficient networking and resource organization.
Declarative configuration is the best practice for managing Kubernetes resources at scale.
