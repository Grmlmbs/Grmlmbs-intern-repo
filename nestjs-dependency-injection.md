nestjs-dependency-injection



#### **6.4 Dependency Injection in NestJS**



**How does dependency injection improve maintainability?**



&#x09;Dependency injection improve maintainability by loosely coupling things so it wouldn't be dependent on how a service is built. Dependency injection also makes changes and testing easier and it makes every provider available for classes to use.



**What is the purpose of the @Injectable() decorator?**



&#x09;@Injectable() makes a class available for participation in dependency injection. Without it, Nest may not register the class as a provider.



**What are the different types of provider scopes, and when would you use each?**



&#x09;Provider scope determines how many instances Nest creates. Nest usually creates different types of provider scopes one of which is DEFAULT it has one instance for the whole app. At most, providers use this for database services, repositories, business services and caches. Another type is REQUEST scope, this is commonly used for request tracking, multi-tenant logic, and request-specific context. The last type is TRANSIENT scope. this scope is used for isolated states, short-lived helpers, and unique object instances.



**How does NestJS automatically resolve dependencies?**

&#x09;

&#x09;To resolve dependencies automatically NestJS first scans the modules and registers them. It then reads the constructor metadata, then builds dependency graph. Lastly, it instantiates the objects automatically in the correct order.

