### Microservices and Kafka

Kafka have a Particion, a each consumer connect on particion

All message are persistence on database, SQLSDB

kafka use a parameter Offset, to determine a quantity of messages already passed, with this offset you can reprocessing a messages from a specific offset. 

With a particion on kafka you can reprocessing the messages of specific topic and specific particion, from a specific offset, so you can reprocessing a messages an specific consumer

Online kafkas to test:
- [confluent.io](https://www.confluent.io/get-started/)
- [cloudkarafka.com](https://www.cloudkarafka.com/plans.html)

![image](https://user-images.githubusercontent.com/12099889/146670971-ac2f0207-d5b5-418b-8b81-f4344f5fa4f3.png)

![image](https://user-images.githubusercontent.com/12099889/146670992-6ad64ae8-ed86-4c7f-b53c-6295cb494fcd.png)

<br>

When a consumer exceeds particion quantity:

![image](https://user-images.githubusercontent.com/12099889/146671355-54b4f760-2679-45cf-be9b-67f96d721bbe.png)

<br>

**Kafka x AMQP**
- Kafka messages expire, after consuming on particion
- Kafka not delete messages after read, so you can reprocessing
- Kafka use a TCP protocol, not use protocol AMQP
- Kafka use a publish-subscripton pattern, AMQP support pub-sub and point-to-point patterns
- AMQP is more easy when you need a routing messages (Exchange Bind to specific Queue)
- Kafka not use a concepts Exnchage, Bind, Queues
- Kafka by default guarantee a message orders (benefies to use a offset kafka), consumer receive messages in the same order has been published, AMQP have a any consumer to a same queue, this not guarantee a messages orders

<br>

**When use Kafka or AMQP**
- Kafka is recomended when you have a big number of messages by second, for example 50K per second, 
- kakfka have a unlimited scalability because use a Topic - Particion
- Kafka is recomended when you need a analytics a events, using a Log Aggregation or Stream (logs in real time)
- Kafka have a ordered messages to reprocessing in a specific consumer

