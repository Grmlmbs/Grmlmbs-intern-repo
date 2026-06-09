typeorm-migrations



#### **7.5 Seeding \& Migrations in TypeORM**



**What is the purpose of database migrations in TypeORM?**



&#x09;Migrations ensure that database is changeable, scalable and eliminates issues that comes from updating and changing databases. TypeORM migrations also tracks database schema changes, applies in a controlled an repeatable manner, keep environments safe and allows safe upgrades and rollbacks.



**How do migrations differ from seeding?**



&#x09;Seeding is the process of inserting data on a database it is done usually to create initial data that a user could use if we have a fresh system while migrations are the process of transferring data from one database to another.



**Why is it important to version-control database schema changes?**



&#x09;Version-controlling is important as we can't still ensure what could break on a system when creating different changes. So, this way we can safely revert to older versions if ever changes still needs fixing and optimizations.



**How can you roll back a migration if an issue occurs?**



&#x09;If an issue occurs, we can roll back a migration by reverting the changes back to its previous states. 

