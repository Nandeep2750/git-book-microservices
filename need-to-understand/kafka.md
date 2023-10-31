# Kafka

## What is Kafka? <a href="#what_is_docker.3f" id="what_is_docker.3f"></a>

Kafka is an open-source **distributed event streaming platform** developed by LinkedIn and later contributed to the Apache Software Foundation. It is designed to handle high-throughput, real-time data streams and offers a robust, scalable, and fault-tolerant architecture. Kafka is primarily used for **building real-time data pipelines and streaming applications**.

## Use cases of Kafka:

1. <mark style="background-color:purple;">**Real-time Data Streaming:**</mark> Kafka is often used as a central hub for real-time data streams. It can **handle high volumes of data**, making it suitable for use cases like log aggregation, telemetry data, social media feeds, sensor data, etc.
2. <mark style="background-color:purple;">**Data Integration:**</mark> Kafka **acts as a messaging system**, allowing different applications and services to communicate and share data in a decoupled manner. It helps integrate diverse data sources and systems.
3. <mark style="background-color:purple;">**Event Sourcing:**</mark> Kafka can be used in **event-driven architectures**, where events represent changes or updates to the system's state. Event sourcing stores these events and allows the system to rebuild its state at any point in time.
4. <mark style="background-color:purple;">**Stream Processing:**</mark> Kafka supports stream processing frameworks like Apache Kafka Streams and Apache Flink. It allows us to analyze data as it comes in, helping us quickly make decisions based on fresh information.
5. <mark style="background-color:purple;">**Message Queues:**</mark> Kafka can act as a high-throughput, fault-tolerant message queue, ensuring reliable delivery of messages between systems. It ensures **messages are delivered safely and quickly**, just like how a reliable mail service makes sure your letters reach the right address.
6. <mark style="background-color:purple;">**Change Data Capture (CDC):**</mark> Kafka can be **used to capture data changes from databases** and feed them into downstream systems for further processing or analytics.

{% embed url="https://youtu.be/uvb00oaa3k8" %}

## Here's how Kafka works

Imagine Kafka as a super-fast and reliable messaging system that allows different applications and services to talk to each other. It's like a central hub where you can send and receive messages.

1. **Topics**: Think of topics as different chat rooms. Each chat room is dedicated to a specific type of conversation. For example, there's a chat room for weather updates, another for news, and so on.
2. **Producers**: These are like messengers who send messages to the chat rooms (topics). They put information into the right chat room for others to read.
3. **Consumers**: Consumers are like people who join the chat rooms and read the messages sent by the messengers (producers). They stay updated with the latest information in their favourite chat rooms.
4. **Brokers**: These are the organisers of the chat rooms. They manage the messages, make sure they are saved properly, and deliver them to the right people.
5. **Partitions**: Imagine each chat room divided into sections called partitions. Each partition stores a part of the messages for that chat room. This helps keep things organised.
6. **Consumer Groups**: People in the chat rooms might belong to different groups, like friends, family, or colleagues. Each group reads messages from specific partitions, so they don't miss any important news.

{% embed url="https://youtu.be/aj9CDZm0Glc" %}

## APIs of Kafka

In Kafka, APIs (Application Programming Interfaces) are available to interact with the system and perform various operations. There are mainly four key APIs in Kafka:

1. **Producer API**: This API allows applications to produce (send) data to Kafka topics. Producers create records (messages) and send them to a specified topic in Kafka. The records are then stored in Kafka and made available to consumers.
2. **Consumer API**: The Consumer API enables applications to consume (read) data from Kafka topics. Consumers subscribe to one or more topics and receive records sent by producers. They can process the data in real-time or use it for various applications like analytics, monitoring, etc.
3. **Streams API**: The Streams API enables stream processing directly within Kafka. It allows developers to build real-time data processing applications and transformations on data streams. With this API, data can be processed, aggregated, or joined before being written back to Kafka topics or sent to other external systems.
4. **Connector API**: This API allows for integration with external systems and data sources. Connectors enable easy and efficient transfer of data between Kafka topics and other storage systems, databases, or data sinks. For example, you can use connectors to move data from Kafka to Elasticsearch, Hadoop, or a relational database.

These APIs provide the necessary functionalities to build robust, scalable, and distributed streaming applications using Kafka. They offer a powerful way to interact with Kafka and leverage its capabilities for various data streaming use cases. Additionally, Kafka also provides a variety of client libraries in different programming languages (Java, Python, etc.) to help developers work with these APIs efficiently in their preferred language.

## How Kafka works with services (Everything you need to know about Kafka)

{% embed url="https://youtu.be/vHbvbwSEYGo" %}

## Kafka Installation

### Kafka installation using Docker and Docker Compose

{% embed url="https://youtu.be/WnlX7w4lHvM" %}
