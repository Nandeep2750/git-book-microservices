---
description: Implementation strategies
---

# Approaches to implement microservices

## Implementation of microservices

Certainly! Let's dive into each method of implementing microservices in more detail using simpler language:

## New Projects:

### <mark style="background-color:purple;">**Greenfield Approach**</mark>

* This means **starting a project from scratch using microservices**. Instead of building one big application, you **build smaller, independent services that perform specific functions**. **Each service can be developed and deployed separately**, making it easier to manage and scale. It's like constructing a building block by block, where each block represents a microservice.

### <mark style="background-color:purple;">**Domain-Driven Design (DDD)**</mark>

* With DDD, you focus on different areas or domains within your project. For example, if you're building an e-commerce website, you might have domains like product management, order processing, and customer management. **Each domain becomes a microservice, allowing you to develop and update them independently**. It's like organizing your project into smaller teams, each responsible for a specific area.

### <mark style="background-color:purple;">**API Gateway**</mark>

* An **API gateway acts as a central point for clients** (such as web or mobile applications) to interact with your microservices. It receives requests from clients and routes them to the appropriate microservice. **This simplifies the client's interaction by providing a single entry point. It's like having a receptionist at the entrance of a building who directs visitors to the correct department.**

<figure><img src="../.gitbook/assets/API Gateway.png" alt="" width="533"><figcaption><p>API Gateway</p></figcaption></figure>

## Existing Projects (Monolithic):

### <mark style="background-color:purple;">**Strangler Pattern**</mark>

*   The strangler pattern is about **gradually replacing parts of your existing monolithic application with microservices**. Instead of rewriting everything at once, you identify specific functionalities that can be extracted and developed as separate microservices. Over time, these microservices take over more and more of the application's functionality, while the monolith becomes smaller. **It's like replacing sections of an old road with new lanes, eventually transforming it into a completely different road.**\
    \


    <figure><img src="../.gitbook/assets/Strangler Pattern.png" alt="Strangler Pattern" width="540"><figcaption><p>Strangler Pattern</p></figcaption></figure>

### <mark style="background-color:purple;">**Modularization**</mark>

* Modularization involves **breaking down your monolithic application into smaller, more manageable modules**. Each module represents a distinct piece of functionality. **You can then refactor these modules into separate microservices that can communicate with each other through well-defined interfaces**. It's like organizing a messy room by categorizing items into different boxes and storing them separately.

### <mark style="background-color:purple;">**Backend-for-Frontend (BFF) Pattern**</mark>

*   In this pattern, you introduce a **"Backend-for-Frontend" service, which sits between your client applications and the monolithic backend.** The BFF service acts as a translator, taking requests from clients and communicating with the monolithic application on their behalf. Over time, you can gradually migrate functionality from the monolithic backend into separate microservices within the BFF. It's like having a dedicated assistant who understands both the clients and the main office, facilitating communication between them.\


    <figure><img src="../.gitbook/assets/Backend-for-Frontend (BFF) Pattern.png" alt="Backend-for-Frontend (BFF) Pattern" width="496"><figcaption><p>Backend-for-Frontend (BFF) Pattern</p></figcaption></figure>



These approaches provide different strategies for implementing microservices based on whether you're starting a new project or working with an existing monolithic application. **Each approach allows for better scalability, maintainability, and flexibility in developing and evolving your software.**

## A few more methods for implementing microservices:

### <mark style="background-color:purple;">**Event-Driven Architecture**</mark>

* Event-Driven Architecture (EDA) is a way of building software systems where **different components communicate by using events**. Events are like notifications that something important has happened. **Instead of components directly talking to each other, they publish events when something occurs, and other components that are interested can listen and respond to those events.**
*   The benefit of EDA is that it allows components to be **independent and loosely coupled**. They **don't need to know about each other's internal details**. When an event happens, only the components interested in that event need to take action, while others can ignore it. This makes the system more scalable, flexible, and easier to maintain.\


    <figure><img src="../.gitbook/assets/Event-Driven Architecture.png" alt="Event-Driven Architecture"><figcaption><p>Event-Driven Architecture<br></p></figcaption></figure>

### <mark style="background-color:purple;">**Saga Architecture (Choreography vs. Orchestration)**</mark>

*   These are two different approaches to managing the flow of activities across microservices. **In choreography, each microservice knows its role and communicates directly with other microservices** to achieve the desired outcome. **In orchestration, a central component (orchestrator) controls and coordinates the interaction between microservices**. Both approaches have their advantages, and the choice depends on the complexity and requirements of your system.

    * **Choreography:** Decentralised co-ordinations where each Microservice produces and listen to other Microservice’s events/messages and decides if an action should be taken or not.
    * **Orchestration:** Centralised co-ordinations where an Orchestrator tells the participating Microservices which local transaction needs to be executed.

    <figure><img src="../.gitbook/assets/Saga Architecture.png" alt="" width="496"><figcaption><p>Saga Architecture</p></figcaption></figure>

{% embed url="https://youtu.be/WnZ7IcaN_JA?t=25" %}

### <mark style="background-color:purple;">Serverless Architecture</mark>

* Serverless computing **allows you to build and run applications without managing the underlying infrastructure**. With microservices, you can leverage serverless platforms (e.g., **AWS Lambda, Azure Functions**) to implement individual microservices. This approach provides scalability, cost efficiency, and automatic scaling based on demand.

### <mark style="background-color:purple;">**Micro Frontends**</mark>

* This method **extends the microservices concept to the frontend of an application**. Instead of building a monolithic frontend, you **decompose the user interface into smaller, independent frontend modules or micro frontends**. Each **micro frontend can be developed and deployed separately, enabling independent development and scalability.**

<figure><img src="../.gitbook/assets/Micro Frontend.png" alt="" width="563"><figcaption><p>Micro Frontends</p></figcaption></figure>

### <mark style="background-color:purple;">**CQRS (Command Query Responsibility Segregation)**</mark>

*   CQRS is an architectural pattern that **separates read and write operations into separate components**. With microservices, you can implement CQRS by having **dedicated microservices for reading data (query) and writing data (command).** This pattern allows for better performance, scalability, and flexibility in handling different types of operations.\
    \


    <figure><img src="../.gitbook/assets/Command Query Responsibility Segregation.png" alt="" width="563"><figcaption><p>Command Query Responsibility Segregation</p></figcaption></figure>

{% hint style="warning" %}
This pattern is usually sufficient for **small and medium-sized applications**, **it may not be the best choice for larger**, more complex applications. In such cases, the **CQRS** model may be more appropriate and scalable (depending on the application's requirements). Benefits of this model include:

* **Separation of concerns**. The model separates the read and write operations into separate models.
* **Scalability**. The read and write operations can be scaled independently.
* **Flexibility**. The model allows for the use of different data stores for read and write operations.
* **Performance**. The model allows for the use of different data stores optimized for read and write operations.
{% endhint %}



{% embed url="https://youtu.be/DQ3D_mplIgY" %}

These additional methods provide alternative approaches and patterns to implement microservices, catering to specific requirements and scenarios. Depending on your project's needs, you can choose the most suitable method or combine multiple approaches to build a robust microservices architecture.

### Summary

{% hint style="info" %}
Here are the names of various approaches to implement microservices:

1. Greenfield Approach
2. Domain-Driven Design (DDD)
3. API Gateway
4. Strangler Pattern
5. Modularization
6. Backend-for-Frontend (BFF) Pattern
7. Event-Driven Architecture
8. Choreography vs. Orchestration
9. Serverless Architecture
10. Micro Frontends
11. CQRS (Command Query Responsibility Segregation)

These approaches offer different strategies and patterns for designing and implementing microservices based on specific requirements, architectural considerations, and project contexts.
{% endhint %}

{% hint style="success" %}
### Which approach among the ones listed above is considered the best for implementing microservices, and why is it considered the best?

It's challenging to declare a single "best" approach from the given options, as the choice depends on the specific requirements, context, and constraints of each project. However, I can provide insights on two popular approaches that are often considered highly valuable in implementing microservices:

* **Domain-Driven Design (DDD):** DDD is a powerful approach that emphasizes understanding and modelling the business domain in software design. It promotes identifying bounded contexts and developing microservices around those domains. By aligning the software architecture with the business domain, DDD can lead to a more maintainable and scalable system. DDD helps to capture complex business logic effectively and fosters collaboration between domain experts and developers.
* **Event-Driven Architecture:** Event-Driven Architecture (EDA) focuses on building systems where components communicate and react to events. This approach enables loose coupling and scalability, as components can react to events asynchronously and independently. EDA is beneficial in scenarios where systems have varying levels of complexity and require real-time event-driven interactions. It promotes responsiveness, agility, and the ability to evolve the system over time.

Both DDD and EDA offer significant benefits for microservices architectures, but the choice of the best approach depends on the specific requirements, complexity, and goals of your project. It's recommended to evaluate each approach against your project's needs and constraints to determine which approach aligns best with your objectives. Additionally, combining multiple approaches or adapting them to suit your project's unique requirements may result in the most effective solution.
{% endhint %}
