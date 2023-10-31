# Some more about architectures

## Types of architecture

We have three types of architectures available:

### Monolithic architecture

* Simple application design as a single piece of code.
* Difficult to maintain, evolve, and scale with complex systems.

<figure><img src="../.gitbook/assets/Monolithic Architecture.png" alt=""><figcaption><p>Monolithic Architecture</p></figcaption></figure>

* Separation of application components into layers based on technical functions.
* Three-tier architecture: presentation, logical, and data layers.
* Centralised design, still not suitable for complex applications.

### Multi-tier architecture

Applications software Engineers propose the solution to this complexity problem by the multi-tier architecture.

* Separation of application components into layers based on technical functions.
* Three-tier architecture: presentation, logical, and data layers.
* Centralised design, still not suitable for complex applications.

<figure><img src="../.gitbook/assets/Multi-tier Architecture.png" alt=""><figcaption><p>Multi-tier Architecture</p></figcaption></figure>

### Microservices architecture

* Evolution of application design from monolithic to multi-tier to microservice-based architectures.
* A popular architectural paradigm addressing limitations of legacy applications.

<figure><img src="../.gitbook/assets/Microservices architecture.png" alt=""><figcaption><p>Microservices architecture</p></figcaption></figure>

#### Introduction to Microservices:

* Breaking down logic and data layers into smaller pieces.
* Microservices handle one business function independently.
* Simple APIs and lightweight protocols for communication
* Enables separate and independent work by different teams.

#### Scaling Microservices:&#x20;

When an organisation adopts microservices architecture, the number of microservices can become quite large. However, **with a large number of microservices, it becomes challenging to identify and fix issues.**

As microservices are distributed and independent, if one microservice fails, it can potentially impact others that rely on it. This makes it difficult to determine the root cause of problems and fix them quickly.

**To manage this complexity**, organizations utilise various tools and techniques. **Containerization tools like Docker help deploy and manage microservices efficiently.** Container orchestration systems like **Kubernetes ensure scalability and fault tolerance.**

**Pipeline automation tools** automate the process of building, testing, and deploying microservices, enabling continuous integration and deployment.

**Asynchronous messaging tools**, such as **message brokers and queues**, facilitate communication between microservices in a decoupled manner.

**Application performance monitoring** tools track the performance of microservices, helping to detect and resolve bottlenecks.

**Logging and audit tools** provide visibility into microservices activities and events, aiding in troubleshooting and ensuring compliance.

These tools and practices help organizations effectively **handle the challenges that arise with a large number of microservices, ensuring smooth operations and quick issue resolution.**

<figure><img src="../.gitbook/assets/Tools for Microservice-based Systems.png" alt=""><figcaption><p>Tools for Microservice-based Systems</p></figcaption></figure>

#### Tools for Microservice-based Systems:

* Containerization (e.g., Docker) for deployment.
* Container orchestration (e.g., Kubernetes) for managing containers.
* Pipeline automation tools (e.g., Jenkins, GitLab CI/CD) for continuous integration and continuous deployment (CI/CD).
* Asynchronous messaging tools (e.g., RabbitMQ, Apache Kafka) with message brokers and queues.
* Application performance monitoring tools (e.g., Prometheus, New Relic, Datadog) for tracking microservice performance.
* Logging and audit tools (e.g., ELK Stack, Splunk) to monitor and track system activities and events.\


{% embed url="https://youtu.be/lL_j7ilk7rc" %}
evolution of application design: from monolithic to multi-tier to microservice based architectures
{% endembed %}
