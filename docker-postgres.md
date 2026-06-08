docker-postgres



#### **5.3 Running PostgreSQL in Docker**



**What are the benefits of running PostgreSQL in a Docker container?**



&#x09;Running PostgreSQL in a Docker container gives you a clean, isolated database environment without installing it directly on your machine. This makes development much more flexible and makes development and testing easier.



**How do Docker volumes help persist PostgreSQL data?**



&#x09;Container data is temporary, If PostgreSQL writes data the container and you delete it, the data is gone. With volumes, data can persists and without it database is reset every time container is removed.



**How can you connect to a running PostgreSQL container?**

&#x09;

&#x09;Once a PostgreSQL container is running, you can connect by using the command docker exec -it pg psql -U postgres. and this would connect your PostgreSQL container that is running on the machine.

