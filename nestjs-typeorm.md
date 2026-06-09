nestjs-typeorm



#### **7.4 Connecting to PostgreSQL with TypeORM in NestJS**



**How does @nestjs/typeorm simplify database interactions?**



&#x09;nestjs/typeorm simplify database interactions by automatically connecting the system to the database so that instead of manually creating the database connection, the nestjs/typeorm handles it and you simply just needs to inject it to your system to work.



**What is the difference between an entity and a repository in TypeORM?**



&#x09;Entity is all about how a data is shaped and how the data looks while repository is how you interact with that data using logic and queries. They were related as the entity is used by the repository and the repository needs the entity to be correct and well formed so it would function properly.



**How does TypeORM handle migrations in a NestJS project?**

&#x09;

&#x09;TypeORM handles migrations as version-controlled database changes that are executed outside your application code, but are tightly integrated through the TypeORM CLI or Nest scripts. The migration is the file that describes how to change the database and how to revert the change done in the database.



**What are the advantages of using PostgreSQL over other databases in a NestJS app?**



&#x09;Using PostgreSQL in a NestJS app isn't mandatory, but it's often preferred for production systems because it's more powerful and stricter than many other relational databases. The real advantage comes from how well it handles other data heavy applications. 



