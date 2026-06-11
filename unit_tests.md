unit\_tests



#### **9.2 Mocking API Calls in Jest**



**Why is it important to mock API calls in tests?**



&#x09;Mocking API calls in tests lets you test your code reliably without depending on real external services, this makes test faster, reliable, makes testing edge cases easier, avoids real side effects, saves const and rate limits and focuses the tests on you code and not the external systems.



**What are some common pitfalls when testing asynchronous code?**



&#x09;Some common pitfalls when testing asynchronous code is not waiting async operations, mixing async/await with callbacks incorrectly, Not waiting for promises inside loops, ignoring timers, Not mocking async external calls, race conditions in tests, shared state between tests, overusing real delays and testing implementation instead of behavior.

