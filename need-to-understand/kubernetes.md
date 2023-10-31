# Kubernetes

## What is Kubernetes?

Kubernetes is an **open-source container orchestration** platform designed to **automate the deployment, scaling, and management of containerized applications.** It was originally developed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF). Kubernetes is commonly abbreviated as **K8s**, where "8" stands for the eight letters between the "K" and the "s."

In the context of modern software development, applications are often divided into smaller, independent components known as microservices. These microservices are typically packaged into containers, which encapsulate all the required dependencies to run the application. Containers are lightweight and provide consistency across various environments, making it easier to deploy and manage applications.

## Use cases of Kubernetes

Kubernetes takes care of the complexities of deploying and managing these containerized applications at scale. Some key features of Kubernetes include:

1. **Container Orchestration:** Kubernetes excels at orchestrating containerized applications, ensuring they run efficiently and reliably across a cluster of machines.
2. **Auto Scaling:** Kubernetes can dynamically adjust the number of containers running based on demand, ensuring the right amount of resources are available to handle incoming traffic.
3. **High Availability:** Kubernetes maintains high availability by automatically distributing containers across multiple nodes, ensuring that your applications stay up and running even if some nodes fail.
4. **Load Balancing:** Kubernetes automatically distributes incoming network traffic across multiple instances of a container, ensuring even distribution and high availability.
5. **Self-Healing:** Kubernetes constantly monitors the health of containers and can automatically restart or replace failed containers to maintain application reliability.
6. **Service Discovery and Networking:** Kubernetes allows containers to discover and communicate with each other through services and provides network solutions for inter-container communication.
7. **Configuration Management:** Kubernetes allows you to define and manage the configuration of applications and their environments separately from the application code.
8. **Rolling Updates and Rollbacks:** Kubernetes enables seamless updates of applications, allowing you to deploy new versions without downtime. If there are issues with the update, Kubernetes supports rolling back to a previous version.
9. **Batch Processing:** Kubernetes can efficiently manage batch workloads, such as data processing and analytics jobs, through its Job and CronJob resources.
10. **Security:** Kubernetes offers various security features, such as role-based access control (RBAC), network policies, and secrets management, to ensure the security of your applications and infrastructure.
11. **Multi-Cloud and Hybrid Environments:** Kubernetes is cloud-agnostic, meaning it can run on various cloud providers or on-premises infrastructure, enabling multi-cloud and hybrid cloud deployments.

## **Kubernetes Architecture**

The diagram below illustrates the many components that make up the K8s architecture. A description of each of the core components follows.

### **Master Node**&#x20;

The master node is responsible for managing the entire Kubernetes cluster. It consists of several components:

1. **API Server:** The API server is the central **control point for the Kubernetes cluster**. It exposes the Kubernetes API, which allows users and other components to **interact with the cluster.**
2. **Etcd:** Etcd is a distributed key-value store that **holds the cluster's configuration data**, representing the state of the cluster at any given moment.
3. **Controller Manager:** The controller manager runs various controllers that handle different aspects of the cluster, such as node management, replication, and endpoints.
4. **Scheduler:** The scheduler is responsible for placing pods (the smallest deployable units in Kubernetes) onto suitable worker nodes based on resource requirements and constraints.

### **Worker Nodes**&#x20;

The worker nodes are the machines where your containerized applications run. Each worker node has the following components:

1. **Kubelet:** Kubelet is **responsible for communicating with the master node** and managing the containers running on its node.
2. **Container Runtime:** The container runtime, such as Docker or containerd, is responsible for pulling and running containers based on the pod specifications from the master.
3. **Kube-proxy:** Kube-proxy is a **network proxy that handles network routing** for services and performs load balancing across the pods.

<figure><img src="../.gitbook/assets/Kubernetes Architecture.png" alt="" width="375"><figcaption><p>Kubernetes Architecture</p></figcaption></figure>

In the diagram, you can see the master node at the top, which consists of the API server, etcd, controller manager, and scheduler. The worker nodes (Worker 1 and Worker 2) are below the master node, each with Kubelet, Container Runtime, and Kube-proxy components.

The master node manages and controls the worker nodes, ensuring that the desired state of the cluster (specified through Kubernetes objects like deployments and services) is maintained. The worker nodes run the applications in containers as specified in the pods, managed by the master node.

This simplified explanation provides an overview of Kubernetes architecture and its key components. In reality, Kubernetes is more complex and has additional features, but this should give you a good starting point to understand how it works.

{% embed url="https://youtu.be/s_o8dwzRlu4" %}
