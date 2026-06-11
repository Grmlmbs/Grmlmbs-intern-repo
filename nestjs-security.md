nestjs-security



#### **8.4 Security Best Practices in NestJS**



**What are the most common security vulnerabilities in a NestJS backend?\\**



&#x09;Most nestJS security problems come from missing guards, validation and unsafe configurations.

**How does @fastify/helmet improve application security?**



&#x09;It improves security by adding protective HTTP headers that reduce the attack surface of your API in the browser, especially against XSS, clickjacking, and unsafe content execution.



**Why is rate limiting important for preventing abuse?**



&#x09;Rate limiting is essentially limiting how much or how frequent can an API accept a request. By doing this we can ensure that the API doesn't fail from handling too much requests and it we can ensure that it would do it tasks that it is assigned to do first before accepting another.



**How can sensitive configuration values be protected in a production environment?**



&#x09;Sensitive configuration values can be protected by setting up the right guards, authentication and authorization. And we can also secure it by minimizing the times it is being accessed and used as much as possible.

