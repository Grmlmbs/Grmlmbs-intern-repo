docker-debugging



#### **5.4 Debugging \& Managing Docker Containers**



**How can you check logs from a running container?**



&#x09;You can check logs by typing the command docker logs <container\_name> and this would help you check the logs in the container.



**What is the difference between docker exec and docker attach?**



&#x09;The command docker exec runs a new command inside the container. It starts a new process inside the container, gives you a shell or runs a command and does not interfere with the main app. On the other hand, docker attach command will attach you to the main process. It connects to the main running process (PID 1), shows stdout/stderr of that process and you are "inside" its live session.



**How do you restart a container without losing data?**

&#x09;

&#x09;To do that, we use docker restart api. This command stops the container, starts it again, and does not delete it hence the data remains safe and persistent.



**How can you troubleshoot database connection issues inside a containerized NestJS app?**



&#x09;To troubleshoot database connection issues inside a containerized NestJS app, you first have to check if DB container is running. You then check for the logs to identify what kind of error has caused the issue. We check the connection string if it is correct or there are any errors or missing details. Once that's done we can verify networking and check if backend APIs are connecting properly. If that works, we check the Postgres' readiness, validate credentials and lastly, check port exposure if needed.

