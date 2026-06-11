nestjs-env-config



#### **8.2 Handling Environment Variables \& Configuration in NestJS**



**How does @nestjs/config help manage environment variables?**



&#x09;It helps manage environment variables by centralizing them. It loads them, validates them, makes them injectable and organizes the configuration intro a structured module.



**Why should secrets (e.g., API keys, database passwords) never be stored in source code?**



&#x09;Because source codes are accessed by others or can be accessed by others, this is actually a common issue with beginners just like me and I commonly see it online being memed in and clowned on by other experienced developers. That is why it should be stored in the source code, It can be stolen and it can make your backend be susceptible from hacking and data breaches. 



**How can you validate environment variables before the app starts?**



&#x09;In NestJS, you can validate environment variables before the app fully starts by using the @nestjs/config with validation schemas. This ensure you app fails fast if something is misconfigured. 



**How can you separate configuration for different environments (e.g., local vs. production)?**



&#x09;It can be done by separating environments by loading different .env files based on NODE\_ENV, and NestJS ConfigModule handles injecting the correct configuration into your app.

