# Microservices architecture

## What is Microservices architecture?

> In a microservices-based deployment, each application function becomes its own service deployed in a container, communicating with each other through APIs.&#x20;

### Advantages of using microservices:

1. **Language and Framework Independence:** Different teams can use their preferred language and framework for their respective services, allowing them to choose the best fit for their requirements.
2. **Faster Iteration:** The use of DevOps pipelines enables rapid iteration and deployment of code into production, independent of the speed of other teams. This allows for faster delivery of value to customers.
3. **Reduced Risk:** If a change or issue occurs in one service, it does not cause the entire application to fail. The microservices architecture allows for smaller, isolated changes, minimising the impact on the overall system.
4. **Modular Scalability:** The architecture allows for the addition of new components over time, which can be written in different languages and frameworks. The services communicate with each other via APIs, facilitating integration.
5. **Independent Scaling:** Microservices provide the ability to scale individual services independently based on the demand. Additional containers can be spun up during peak loads and removed when the load subsides, enabling the application to scale naturally.

{% hint style="success" %}
### Summarized advantages of using microservices

In summary, the microservices architecture offers language independence, faster iteration, reduced risk, modular scalability, and independent scaling, making it an appealing approach for building applications.
{% endhint %}
