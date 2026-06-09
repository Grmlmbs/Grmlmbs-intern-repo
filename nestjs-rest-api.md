nestjs-rest-api



#### **7.1 Creating REST APIs with NestJS**



**What is the role of a controller in NestJS?**

&#x09;

&#x09;Controllers defines API endpoints, it is the one responsible for receiving requests, validating inputs, call services and return responses needed inside the app.



**How should business logic be separated from the controller?**



&#x09;There should be a separation of responsibility and features should be grouped by what they were supposed to do. Business logics should be inside the service layer and as it is the one that would process the data received through the controllers and apply rules on them as intended.



**Why is it important to use services instead of handling logic inside controllers?**



&#x09;Services contains all logic that is needed to process the data received. By separating it from the controller, we can ensure that we are only handling clean data that came from the controller and we can narrow down possible variables that might cause error and only expect them to happen on their specific layer.



**How does NestJS automatically map request methods (GET, POST, etc.) to handlers?**



&#x09;It maps them by the use of metadata, decorators and HTTP methods.

