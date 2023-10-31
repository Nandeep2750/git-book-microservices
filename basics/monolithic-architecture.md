# Monolithic architecture

## What is Monolithic architecture?

> A monolith is a **server-side system based on a single application.**

* **Initially, it's easy to develop, deploy, and manage.**

To get a better understanding through an example. In this case, let's pretend we're a ticketing platform and we sell tickets to sporting events and concerts. which has given components...

Firstly, there would be a **user interface**, which allows users to interact with the platform. Another important component is the **inventory system**, which manages the available tickets. The system also includes a **recommendation generator** that suggests tickets based on user input. Additionally, there would be a **cart for users** to store their selected tickets before making a purchase. A **payment** and **ordering component** handles the financial transactions, and a reporting engine generates **reports** on various aspects of the platform's operations.

### Challenges with monolithic architectures:

* **High Dependency on Shared Libraries:** Changes to one library can have extensive ramifications on the entire application, potentially bringing down the system during updates.
* **Lack of Flexibility in Frameworks and Languages:** Once a monolith is built with specific technologies, additional components must also be developed using the same technologies, even if better alternatives exist.
* **Difficulty Understanding the Growing System:** As the application expands, it becomes increasingly challenging for the development team to comprehend the entire system, leading to deployment and maintenance issues.
* **Complex and Time-Consuming Deployments:** Deploying a monolith, especially as it grows, requires implementing deployment windows and stabilising the system before peak usage periods, which can be a complex and time-consuming process.
* **Scalability Concerns:** Monolithic architectures face challenges in handling scalability, such as surges in demand that strain components like the payment system, requiring time-consuming redeployment and potentially missing peak demand periods.

{% hint style="warning" %}
**summarized challenges with monolithic architectures:** Monolithic architectures have challenges of high dependency on shared libraries, limited flexibility in frameworks and languages, difficulty in understanding the growing system, complex and time-consuming deployments, and scalability concerns. These challenges impact the deployment process and the ability to deliver a seamless user experience.
{% endhint %}

As a result of the above issue in Monolith, we will encounter similar issues in our example platform.

* Even if there is a better alternative, we cannot use new technologies and tools throughout the application.
* In this application, the scope of the application and user inputs will grow over time, making it difficult to manage and explain to the team how this works and how modules work.
* Also, deployment will be more difficult, and we will need to test the application even if we only changed one feature.
* If the platform becomes overcrowded and a large number of people attempt to purchase tickets, and we encounter a payment issue, we must redeploy the app. We are unable to add additional payment services.
