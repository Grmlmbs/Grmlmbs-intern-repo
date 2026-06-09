nestjs-validation



#### **7.2 Validating Requests with Pipes in NestJS**



**What is the purpose of pipes in NestJS?**



&#x09;Pipes are classes that validates inputs before controllers handles them. This way we can ensure that we are handling data with the correct format and it can be safely processed by the other layers.



**How does ValidationPipe improve API security and data integrity?**



&#x09;ValidationPipe checks if the input received is valid and rejects it if it isn't. This way we can ensure that what comes in the system for processing is only data that the system can handle and data can stay consistent.



**What is the difference between built-in and custom pipes?**



&#x09;Built-in pipes are premade pipelines that NestJS already has and provide while custom pipes are pipes that the developer himself creates and sets.



**How do decorators like @IsString() and @IsNumber() work with DTOs?**



&#x09;These decorators checks if data follows a certain criteria or rule, if it flags it no then it would be handled first either for transforming or it would be rejected by the system.





