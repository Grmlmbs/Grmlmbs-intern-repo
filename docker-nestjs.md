docker-nestjs



#### **6.6 Using Docker for NestJS Development**



**How does a Dockerfile define a containerized NestJS application?**



&#x09;A docker file is the instructions Docker follows to build an image. For a NesJS app, it defines; the base environment, dependencies, source code, build process and startup command.



**What is the purpose of a multi-stage build in Docker?**



&#x09;Multi-stage builds separate build environment from runtime environment to create smaller, cleaner and safer production images.



**How does Docker Compose simplify running multiple services together?**



&#x09;It simplifies it by centralizing configurations and providing a place for the entire stack to be controlled altogether.



**How can you expose API logs and debug a running container?**



&#x09;To debug a running container you usually follow this steps:



&#x09;**Step 1:** View logs

&#x09;**Step 2:** Enter container

&#x09;**Step 3:** Inspect the running processes

&#x09;**Step 4:** Test connectivity

&#x09;**Step 5(optional):** Enable Nest debug mode.

