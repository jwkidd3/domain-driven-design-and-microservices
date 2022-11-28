### Managing Data Integrity

Designer for failure: you can have a failure points in all interfaces, Database, Message Broker, Microsservice, ...

You can use a table in your datebase for registry if a events are seding, follow diagram:

![image](https://user-images.githubusercontent.com/12099889/146111266-011dd1de-b45d-4cff-ae47-f309c29b1968.png)


![image](https://user-images.githubusercontent.com/12099889/146111275-4b675494-9a44-4ded-9876-0f3f207d3f8e.png)

**RabbitMQ** is a solid, general-purpose message broker that supports several protocols such as AMQP, MQTT, STOMP, etc. It can handle high throughput. A common use case for RabbitMQ is to handle background jobs or long-running task, such as file scanning, image scaling or PDF conversion. RabbitMQ is also used between microservices, where it serves as a means of communicating between applications, avoiding bottlenecks passing messages.

**Kafka** is a message bus optimized for high-throughput ingestion data streams and replay. Use Kafka when you have the need to move a large amount of data, process data in real-time or analyze data over a time period. In other words, where data need to be collected, stored, and handled. An example is when you want to track user activity on a webshop and generate suggested items to buy. Another example is data analysis for tracking, ingestion, logging or security.
