nestjs-logging



#### **8.3 Logging \& Error Handling in NestJS**



**What are the benefits of using nestjs-pino for logging?**



&#x09;NestJS-pino is fast and provides very great compatibility while working on production + container setups which many organizations use today. It also have a very structured JSON logs which helps a lot during debugging especially in distributed systems.



**How does global exception handling improve API consistency?**



&#x09;Having global exception handling improve API consistency by removing the need for creating handlers for every controller. This in turn makes APIs run faster and more consistently with a more uniform and manageable error handling when an error occurs.



**What is the difference between a logging interceptor and an exception filter?**



&#x09;Exception filters handles errors while logging interceptors observes requests/responses.



**How can logs be structured to provide useful debugging information?**



&#x09;You can structure in way that it helps debugging by tracking the process and recording the events that happened from that start, in between and up to the last part of the process. It could be by adding concise and descriptive error messages or recording how frequently this occurs so that you can work on mitigating this issues.

