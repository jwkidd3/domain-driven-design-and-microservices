### Events Driven Architecture and Domain Events

**EDA**: Event Driven Architecture

<br>

![image](https://user-images.githubusercontent.com/12099889/145731671-e09a7f78-23b8-4e4e-8adf-0af14d64a5f1.png)

<br>

Event messages may contains _Meta data_ or _State data_

- **State data**
  - Is a complete data with all informations about event, example:
    - Event CustomerCreated: (Id, Name, Surname, Address, ...)         


- **Meta data**
  - Is a basic data with about event, example:
    - Event CustomerCreated: (Id)]
    - In this case, when consulme the event need coonsult a API or service, if need more infomations about new customer   

<br>

![image](https://user-images.githubusercontent.com/12099889/145731924-455ee9af-ef29-45b6-b921-fd88ed557981.png)

**AMQP** is a protocol to comunicate, Advanced Message Queuing Protocol is an open standard application layer protocol for message-oriented middleware

AMQP expose API, used in system with rabbit, kafka to get informations about keys

![image](https://user-images.githubusercontent.com/12099889/145860952-09528f6d-3c73-4532-8fd6-ef72b010f756.png)

![image](https://user-images.githubusercontent.com/12099889/145865423-4ef77d83-f481-4dd5-96c7-0aaa7bd350ef.png)

![image](https://user-images.githubusercontent.com/12099889/145865440-dbd6a364-4b1e-4fb3-b650-dc8de0284c3b.png)


