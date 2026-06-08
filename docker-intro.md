docker-intro



#### **5.1 What is Docker and Why Use It?**



**How does Docker differ from a virtual machine?**



&#x09;Docker runs by using the computer's own OS and environment unlike in virtual machines where you have to allocate those resources for the virtual machine to function as an individual machine separate from the host. This makes docker faster and cheaper to maintain and handle.



**Why is containerization useful for a backend like Focus Bear's?**



&#x09;It is useful because it takes care of the hassles of setting up your machine to accommodate the supposed requirements needed to start developing or working on a backend infrastructure. Instead of installing dependencies manually, you could just setup the docker so it would bring the whole environment for you to use therefore eliminating such hassle.



**How do containers help with dependency management?**



&#x09;Containers are a packaged environment so basically you can call it and use the dependency it is packaged with. If you need an older version of the dependency, you can make a container that has that older dependency and so on. You can also freely delete a container if needed without affecting the other containers. These reasons makes it very manageable, flexible and quite forgiving during development.



**What are the potential downsides of using Docker?**



&#x09;The downside I'm seeing is it would take some time to learn how to use it properly and there would probably be a learning curve to use it. Mainly because of the reason that it runs through network and that on its own can introduce quite a lot of headaches and issues that will take some time figuring especially if it is your first time handling it.

