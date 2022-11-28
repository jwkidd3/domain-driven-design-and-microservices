### Database Performance

Bottleneck = Gargalo

![image](https://user-images.githubusercontent.com/12099889/146069769-d651d120-9e5a-4e63-a313-236b511d9c91.png)

**CQS**: Command Query Separation

**CQRS**: Command Query Responsability Segregation

When you separate a databases to read and write you have a beneficies:
- Your indexes to read, not cause impact in your writes
- Scale, with replicas or shardings, your databases read separated a database write 

![image](https://user-images.githubusercontent.com/12099889/146072256-daf001bf-7ea3-47a4-ac8c-d7a93cc982cf.png)

We can use a Event to inform to another microservice that a new registre is inserted and the subscribe insert the new or updated registre in read dabatase.

Event Store DB: https://www.eventstore.com/

Example MongoDB read DB:

![image](https://user-images.githubusercontent.com/12099889/146074284-29d71ee2-3504-4b2a-bda8-48dc5e1ace26.png)
