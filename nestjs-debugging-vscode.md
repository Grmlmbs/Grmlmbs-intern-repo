nestjs-debugging-vscode



#### **10.3 Debugging with VS Code \& Breakpoints**



**How do breakpoints help in debugging compared to console logs?**



&#x09;Breakpoint are more powerful than console logs because they let you pause execution, inspect live state, and step through code line-by-line, making them ideal for deep debugging, while console logs are better for quick, lightweight checks.



**What is the purpose of launch.json, and how does it configure debugging?**



&#x09;launch.json is a blueprint that tells VS Code exactly how to run and debug your project. When you press F5, VS Code reads this file and start your program based on the config then attaches the debugger. This let's you set breakpoints, step through code, inspect variables, watch expressions and view call stacks.



**How can you inspect request parameters and responses while debugging?**

&#x09;

&#x09;To inspect request/response while debugging using breakpoints, Debug console, interceptors/middleware, network tools and attach debugger.



**How can you debug background jobs that don’t run in a typical request-response cycle?**



&#x09;To debug background jobs you can attach debuggers, put breakpoints in job processors, Use logs for flow tracking, Use queue dashboards, replay failed jobs with same payload, isolate worker process from API and use debugger statement for quick pause.

