---
title: "Exploring the Kubernetes Architecture"
datePublished: Sat Oct 07 2023 16:12:24 GMT+0000 (Coordinated Universal Time)
cuid: clng8hbvy000108l3b9xi99yi
slug: exploring-the-kubernetes-architecture
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696668675428/dac89ddd-5452-454c-94de-71dac59ec99c.jpeg
tags: kubernetes, architecture, devops, devops-articles, the-devops-tales

---

Kubernetes, commonly known as **K8s**, is an open-source platform that has revolutionized the arena of container management. Yet, what is Kubernetes and how does it operate?

In this blog post, we will explore the inner workings of Kubernetes, breaking it down into comprehensible parts to increase our insight into it.

**The Foundation:** Before getting into Kubernetes, let's get to the essence of the matter: "<mark>containers</mark>". Think of containers as specialized boxes that enclose all the important components necessary for software applications to run. These boxes incorporate the code, libraries, and settings that are mandatory for code to run efficiently across diverse surroundings. Containers make it possible to ship and run software seamlessly across different systems without worrying about fitting issues.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696693112665/219ccfaf-9b67-43ee-a67c-60a6520dffa3.jpeg align="center")

### Control Plane Components

1. **API Server:**
    
    Role: Central Hub
    
    The API Server functions as the primary entry point for interacting with a Kubernetes cluster. It exposes the Kubernetes API, permitting users, administrators, and various components to communicate and manage the cluster. Imagine this as the central hub of a city, where all instructions and requests converge.
    
2. **ETCD:**
    
    Role: Memory of the Cluster
    
    Etcd is a distributed key-value store that works as the cluster's memory. This distributed key-value store preserves all the essential information responsible for the configuration and present state of the cluster, just like a city's memory bank. It guarantees that vital data is kept securely and readily accessible.
    
3. **Controller Manager:**
    
    Role: City planner
    
    The controller manager is responsible for maintaining the preferred state of the cluster. It monitors the actual state of the cluster and makes the required adjustments to align it with the preferred state. Imagine this as the city planner ensuring that the buildings, roads, and infrastructure stick to the city's master plan.
    
4. **Scheduler:**
    
    Role: Traffic Manager
    
    The primary responsibility of the Scheduler is to allocate tasks (containers) to individual nodes in the cluster. It makes optimal decisions based on resource availability and constraints. Schematically speaking, this is equivalent to a traffic manager directing vehicles (containers) to the appropriate routes (nodes) to guarantee smooth flow and resource efficiency.
    

### Node Components

1. **Kubelet:**
    
    Role: Worker
    
    Kubelet serves as a worker on each node, tasked with managing containers. It guarantees that any containers running on the node are kept in the prescribed state. Kublet communicates with the control plane to report the node's status and receives instructions, similar to a worker following instructions from the central office.
    
2. **Kube Proxy:**
    
    Role: Network Rule Enforcer
    
    Kube Proxy maintains network regulations for each node. It guarantees that networking regulations, including routing and load balancing, are configured correctly. Think of it as the traffic police of the city, enforcing traffic and maintaining road connections for efficient communication.
    
3. **Container Runtime:**
    
    Role: Container executer
    
    The task of a container executor is to run container images, granting an isolated space for the application to work within. Popular container runtimes include Docker, similar to a chef in a restaurant preparing dishes based on customers' orders.
    

### Key Concepts

1. **Pods:**
    
    Pods are the smallest deployable units in Kubernetes. They contain one or more containers that share the same network and storage. Imagine pods as apartments in which multiple individuals (containers) live together and operate closely.
    
2. **Services:**
    
    Services define a set of pods that create policies for their access. They act as permanent routes for connecting to applications functioning in the cluster, similar to a guidebook or contact list, which helps you pinpoint locations in the city.
    
3. **Volumes:**
    
    Volumes offer a means to store and share data for containers. These are like storage lockers, ensuring data availability for the containers regardless of how often they move or restart.
    
4. **ConfigMaps and Secrets:**
    
    ConfigMaps stores configuration information, such as environment variables and configuration files. Secrets store data that is sensitive, such as passwords and API keys. These resources are essential for configuring and protecting applications.
    

### Security Features

1. **RBAC (Role-Based Access Control):**
    
    Role-Based Access Control (RBAC) provides the cluster with finely tuned permission and access control regulations. It ensures that only authorized users and components can perform specific actions. Much like security systems that grant access-based roles and permissions.
    
2. **Pod Security Policies:**
    
    Pod Security Policies, or PSPs, is an essential component of ensuring a secure container runtime. These policies define restrictions on pod placement and usage in a Kubernetes cluster, as well as the settings that should be applied to each container within a pod. By enforcing secure practices in the cluster, PSPs help protect sensitive data, ensure availability, and keep malicious actors at bay.
    
3. **Network Policies:**
    
    Network Policies control network traffic between pods. They act as security guards, specifying which pods can communicate with each other and under what conditions, enhancing network security within the cluster.
    

In summary, Kubernetes is similar to a highly organized city, with its Control Plane supervising operations and node components performing the hands-on work.

Key concepts like Pods, Services, Volumes, and ConfigMaps make it versatile, while security features like RBAC, PSPs, and Network Policies ensure a safe and secure environment. Understanding these components is crucial for effectively managing Kubernetes clusters and deploying applications at scale.

So, next time, whenever you start with Kubernetes, visualize it as a well-structured metropolis orchestrating containerized applications with precision and efficiency.

---

> I appreciate you reading my blog post! Please think about joining me on [**<mark>LinkedIn</mark>**](https://www.linkedin.com/in/sagar-kumawat/) if you find this information useful and want to stay updated with articles, thoughts, and business contacts. Let's carry on the discussion and build our network together.