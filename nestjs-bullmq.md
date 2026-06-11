nestjs-bullmq

#### **7.6 Background Jobs with BullMQ \& Redis in NestJS**



**Why is BullMQ used instead of handling tasks directly in API requests?**



&#x09;Let's say you want to post a video or upload a video. You upload the video right? But hold on you want to, for now, minimize something to do other things while the video uploads. But you can't because you can't leave while the video is still uploading and the API is still working on it. That is when BullMQ is used, it queues the process and does the uploading in the background. This way, you can immediately give result even though it is technically still on route to finishing. It improves user experience and helps your app function much faster and efficiently.



**How does Redis help manage job queues in BullMQ?**



&#x09;Redis serves as the backend storage for BullMQ, it records states and processes jobs from like queueing, running, completion and also records failures as well as retrying them automatically.



**What happens if a job fails? How can failed jobs be retried?**



&#x09;If a job fails, it can either be retried automatically or retried manually which you can configure while setting up the bullMQ.



**How does Focus Bear use BullMQ for background tasks?**

&#x09;

&#x09;Focus bear might be using this for scheduling the tasks on the app after the user sets some and it might've been also used in the whole backend itself because it uses NestJS for the backend.

