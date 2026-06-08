nestjs-setup



#### **6.2 Setting Up a NestJS Project**



**What files are included in a default NestJS project?**



&#x09;There were a few files along with a src file and inside the src folder there's a controller, a module, service and a main .ts file.



**How does main.ts bootstrap a NestJS application?**



&#x09;The main function of the main.ts file is to start the app, it has the NestFactory inside which builds everything and AppModule which has the blueprints to guide the NestFactory on how to build the app.



**What is the role of AppModule in the project?**



&#x09;The app module serves as the blueprint of the whole application. It serves as the entry point of the architecture, registers components, serves as the container for dependencies and holds other imported modules.



**How does NestJS structure help with scalability?**



&#x09;NestJS has a modular architecture which makes development easier to maintain, manage and scale. It also makes testing more convenient and makes job more flexible and manageable by allowing for the reusability of modules.

