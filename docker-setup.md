docker-setup



#### **5.2 Setting Up Docker and Docker Compose**



**What is the difference between docker run and docker-compose up?**



&#x09;docker run is a single container launcher while docker compose up is a multi-container system launcher. You use docker run when testing a single container, debugging images and quick experiments while docker compose up is used when you are going to work on real projects with complete infrastructure and environments setups.



**How does Docker Compose help when working with multiple services?** 



&#x09;Docker compose helps turn messy set of separate containers into a single, coordinated application environment. Using docker compose will help you ensure that every services that your using in the project works together reliably, consistently and smoothly.



**What commands can you use to check logs from a running container?**



&#x09;For checking logs, we will use docker logs <container name>. we can also target which logs we can view using a few extended commands that we will add along this command.



**What happens when you restart a container? Does data persist?**



&#x09;When a container is restarted the data is just rebooted along with the container but the data still persists after the restart.



