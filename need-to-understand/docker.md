# Docker

## What is Docker? <a href="#what_is_docker.3f" id="what_is_docker.3f"></a>

Docker is an open-source platform that allows you to **build, test, and deploy applications quickly**. Docker packages software into standardized units called **containers** that have everything the software needs to run, including libraries, system tools, code, and runtime.&#x20;

In short, it **automates the deployment, scaling, and management of applications inside lightweight & portable containers**. Containers are a form of virtualization that allows applications to **run in isolated environments**, ensuring that they work consistently across various computing environments.

## How Docker Works <a href="#how_docker_works" id="how_docker_works"></a>

Docker works by providing a standard way to run your code. Docker is an operating system for containers. **Similar to how a virtual machine** virtualizes (removes the need to directly manage) server hardware, containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

\


<figure><img src="../.gitbook/assets/Docker vs VM.png" alt="" width="462"><figcaption><p>Docker vs Virtual Machine</p></figcaption></figure>

## The Key Components of Docker

1. **Docker Engine:** The core component that enables the creation and execution of containers on a host system.
2. **Docker Image:** A lightweight, standalone, and executable software package that includes everything needed to run an application, including the code, runtime, libraries, and dependencies.
3. **Docker Container:** An instance of a Docker image running as a process. Containers are isolated from each other and from the host system, making them portable and secure.

## Docker Architecture <a href="#docker-architecture" id="docker-architecture"></a>

Docker uses a **client-server architecture**. The Docker _client_ talks to the Docker _daemon_, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon _can_ run on the same system, or you can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate using a REST API, over UNIX sockets, or a network interface. Another Docker client is Docker Compose, which lets you work with applications consisting of a set of containers.

<figure><img src="../.gitbook/assets/Docker architecture.png" alt=""><figcaption><p>Docker architecture</p></figcaption></figure>

## Uses of Docker

1. **Application Deployment and Isolation:** Docker allows developers to package applications and all their dependencies into containers. This ensures that the application can run consistently across different environments without worrying about conflicts between dependencies or system configurations.
2. **Portability and Consistency:** Docker containers can be easily moved between different environments, such as development, testing, and production, ensuring consistency and reducing the risk of "it works on my machine" issues.
3. **Scalability:** Docker makes it easy to scale applications by allowing multiple containers to run the same application across multiple hosts, balancing the workload efficiently.
4. **Versioning and Rollbacks:** Docker images can be versioned, allowing for easy rollbacks to previous versions of an application in case of issues with new releases.
5. **Collaboration and Continuous Integration/Continuous Deployment (CI/CD):** Docker facilitates collaboration between developers, testers, and operations teams, as they can work with the same containerized application. It also integrates seamlessly into CI/CD pipelines, making the deployment process faster and more reliable.
6. **Microservices Architecture:** Docker is commonly used in microservices architectures, where each microservice runs in its own container. This approach allows for easy development, testing, and deployment of individual components of an application.
7. **Resource Efficiency:** Containers are lightweight and share the host system's OS kernel, which reduces overhead and allows for greater resource efficiency compared to traditional virtual machines.

## Consider the Following Example Scenario:

* Your developers write code locally and share their work with their colleagues using Docker containers.
* They use Docker to push their applications into a test environment and execute automated and manual tests.
* When developers find bugs, they can fix them in the development environment and redeploy them to the test environment for testing and validation.
* When testing is complete, getting the fix to the customer is as simple as pushing the updated image to the production environment.

## Summary

In summary, Docker simplifies the process of deploying and managing applications, ensures consistency across different environments, and promotes a more efficient and scalable way of developing and delivering software.

{% embed url="https://youtu.be/rOTqprHv1YE" %}

{% embed url="https://youtu.be/gAkwW2tuIqE" %}
