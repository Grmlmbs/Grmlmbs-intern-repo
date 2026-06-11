nestjs-api-debugging



#### **10.4 Inspecting API Requests \& Responses**



**How can logging request payloads help with debugging?**



&#x09;Logging request payloads helps you debug by showing exact input received, making bugs reproducible, exposing frontend/backend mismatches, tracking async or distributed flows and identifying data changes or breaks.



**What tools can you use to inspect API requests and responses?**



&#x09;To help inspect API requests and responses, you can use some tools like Postman, Bruno, VS Code debugger, Chrome DevTools and cURL.



**How would you debug an issue where an API returns the wrong status code?**



&#x09;To debug wrong API status code you can do this; Reproduce with Postman/Bruno, Check controller logic first, Verify thrown exceptions, inspect middleware/interceptors, use breakpoints to trace res.statusCode, Watch async/await issues, confirm framework default behavior and lastly force explicit status codes when needed.



**What are some security concerns when logging request data?**



Logging request data becomes a security risk when it:



* exposes sensitive information.
* is stored too long.
* is accessible to unauthorized users.
* includes internal system details.
* is not properly sanitized.

