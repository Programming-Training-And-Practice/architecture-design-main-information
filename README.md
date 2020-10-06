# Architecture Design.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [General.](#general)
* [Microservice Architecture.](microservice-architecture.md)
* [Event-Driven Architecture.](event-driven-architecture.md)
* [Serverless Architecture.](serverless-architecture.md)
* [Cloud Architecture.](cloud-architecture.md)
* [General Parts.](#general-parts)
* [Situations that can provoke problems on the Server.](#situations-that-can-provoke-problems-on-the-server)
* [Sort This.](#sort-this)
* [Type of Scaling.](#type-of-scaling)
* [Help.](#help)





## About.





## Documentation.
* [The twelve-factor app](https://12factor.net/)





## General.
* [Netflix OSS.](https://www.google.com/search?q=netflix+oss&oq=netflix+oss&aqs=chrome.0.69i59j35i39j0l3j46j0j69i61.1691j0j7&sourceid=chrome&ie=UTF-8)





## General Parts.
* API Gateway.
* Load Balancer.
* Fault Tolerance and Resilience.
* Cycle Breaker Pattern.
* Fallback.
* Config Server.
* Authentication and Authorization. 





## Situations that can provoke problems on the Server.
* Control the number of threads on the server.
* Slow executions of thread.





## Sort This.
> * Fallback functionality.
>> * Throw an error. This way is not recommended.
>> * Return a fallback "default" response.
>> * Save previous responses (cache) and use that when possible.





## Type of Scaling.
* Horizontal.
* Vertical.
* Hybrid.





## Help.
