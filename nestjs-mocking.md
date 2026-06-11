nestjs-mocking



#### **9.7 Mocking Dependencies \& Database Interactions in NestJS**



**Why is mocking important in unit tests?**

&#x09;

&#x09;Mocking is important because unit tests should validate you code's logic in isolation, making tests faster, more reliable, and easier to control.



**How do you mock a NestJS provider (e.g., a service in a controller test)?**



&#x09;In NestJS, you mock a provider by replacing the real dependency with a fake implementation inside Test.createTestingModule(). Using provide + useValue (or useClass / useFactory) so your unit test stays isolated and predictable.



**What are the benefits of mocking the database instead of using a real one?**



&#x09;Mocking the database in unit tests is useful because it lets you test application logic without depending on an actual database. By doing so we can have fast, isolated, and predictable unit tests. While real database are better for integration testing where you want to verify actual data behavior.



**How do you decide what to mock vs. what to test directly?**



&#x09;One thing that I understood so far is that if it is external, slow, and has side effects, you can Mock it. On the other hand, if it is a business logic that you have confidence in you can test it directly.

