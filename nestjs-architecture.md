nestjs-architecture



#### **6.3 Understanding Modules, Controllers, and Providers in NestJS**



**What is the purpose of a module in NestJS?**



&#x09;A module groups related parts of an application together; controllers, providers, imported modules, and exported functionality. It exist to organize code, isolate responsibilities, allow reuse and make scaling easier and without it large apps become difficult to maintain.



**How does a controller differ from a provider?**



&#x09;Controllers receive incoming HTTP requests and send responses. It's responsible for receiving requests, validate input, call services, and return responses. Providers, on the other hand, perform application work. They were responsible for database logic, calculations, authentications and business rules.





**Why is dependency injection useful in NestJS?**



&#x09;Dependency injection(DI) is when objects receive dependencies instead of creating them. It makes components to depend on interfaces/services instead of construction details. It provides Reusability, Centralized lifecycle management and easier testing overall. 



**How does NestJS ensure modularity and separation of concerns?**



&#x09;NestJS achieves this by using several layers. Which are; Layer 1(Modules) which incapsulates the Features. Features are grouped here which has its own components. Layer 2(Controllers) which manages communication, Layer 3(Providers) which handles the behaviors and Lastly, we have Layer 4(Dependency injection) where dependencies were given rather than accessed.

