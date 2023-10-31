# Understand more about Microservices

For those who don't know, we will dive in get some more idea...

> A microservice is an architectural pattern where every application function is its own service, and these services are deployed in containers, and these containers speak with each other via APIs.

### Important points about microservice architecture

Certainly! Here are some additional important points about microservice architecture:

1. <mark style="background-color:purple;">**Scalability:**</mark> Microservices allow applications to scale horizontally, meaning **you can add more instances of a particular service to handle increased load**. This scalability is crucial for applications experiencing rapid growth or fluctuating traffic patterns.
2. <mark style="background-color:purple;">**Independent Deployment:**</mark> Each microservice **can be deployed independently, enabling faster release cycles**. This agility is advantageous for companies that want to iterate and deploy **new features or fixes without affecting the entire application**.
3. <mark style="background-color:purple;">**Technology Diversity:**</mark> Microservices offer the flexibility **to use different technologies for each service** based on its specific requirements. **This freedom allows companies to choose the best tools and frameworks for each service**, resulting in improved performance and development productivity.
4. <mark style="background-color:purple;">**Fault Isolation:**</mark> Microservices are designed to be independent, so if **one service fails or experiences issues, it won't affect the entire application**. This fault isolation ensures that failures are contained within a single service, minimizing the impact on the overall system.

### **List well-known Companies that use microservices**

Now let's look at some well-known companies that use microservices and their reasons for choosing this architecture:

1. <mark style="background-color:purple;">**Netflix:**</mark> Netflix adopted microservices to **handle their massive scale and diverse user base**. Microservices allowed them to **evolve and scale different parts of their system independently**, **improving availability** and **enabling frequent deployments**.
2. <mark style="background-color:purple;">**Amazon:**</mark> Amazon utilises microservices to **power various aspects of their e-commerce platform.** The modular nature of microservices allows Amazon to **quickly experiment with new features**, **optimize performance**, and **handle high traffic during peak shopping seasons**.
3. <mark style="background-color:purple;">**Uber:**</mark> Uber's complex transportation platform relies on microservices for its scalability and flexibility. Microservices enable Uber to **handle millions of ride requests and transactions**, while also allowing them to **integrate with third-party services** and continuously innovate their platform.
4. <mark style="background-color:purple;">**Airbnb:**</mark> Airbnb employs microservices to support their global accommodation marketplace. By breaking down their application into smaller services, Airbnb can **iterate on specific features, improve performance, and seamlessly scale their platform to cater to the growing demands** of travelers and hosts.

These companies chose microservices due to the need for **scalability, independent deployment, technology diversity, fault isolation, and the ability to support their rapid growth and innovation.**

To get better understanding what a microservice is, let's compare it to a monolith. will see monolithic and microservice-based architectures one by one...
