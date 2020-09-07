# Microservice Architecture.





## Contents at a Glance.
* [About](#about)
* [Documentation.](#documentation)
* [Pros.](#pros)
* [Cons.](#cons)
* [Best Practices to Design Microservices.](#best-practices-to-design-microservices)
* [Microservice Architecture most important parts.](#microservice-architecture-most-important-parts)
* [Microservice most important parts.](#microservice-most-important-parts)
* [API Gateway.]()
* [Distributed Transaction Management.]()
* [Versioning.](#versioning)
* [Microservice Challenges.](#microservice-challenges)
* [Characteristics of Microservices.](#characteristics-of-microservices)
* [Issues with microservices.](#issues-with-microservices)
* [Idempotency.](#idempotency)
* [Transaction Compensation.](#transaction-compensation)
* [Useful URL.](#useful-urls)
* [Help](#help)





## About.





## Documentation.





## Pros.
* Polyglot Architecture.
* Freedom to use different technologies, tools, languages.
* Easy scaling for microservices that need scaling.
* Better team management , each microservice is a team.
* Easier to innovate certain areas.
* Each microservice can pick their own database.
* Scale busy service instead of entire system.
* Supports individual deployable units.
* Mulitple services are parallelly developed and deployed.
* Allow frequent software releases.
* Each microservices focuses on single capability.
* Ensures security of each service.
* Independent Development.
* Independent Deployment.
* Fault Isolation.
* Granular Scaling. Individual components can scale as per need, there is no need to scale all components together.






## Cons.
* Very complicated to implement, network call, service discovery.
* Increases troubleshooting challenges.
* Very difficult debug.
* Hard to find where the fault is.
* Network calls fails adds complexity.
* Increases delay due to remote calls.
* Increased efforts for configuration and other operations.
* Difficult to maintain transaction safety.
* Tough to track data across various boundaries.
* Difficult to code between services.





## Best Practices to Design Microservices.
* Separate date store for each Microservice.
* Keep code at a similar level of maturity.
* Separate build for each Microservice.
* Deploy into container.
* Treat servers as stateless.





## Microservice Architecture most important parts.
* API Gateway.
* Circuit Breaker.
* Load Balancing.
* Distributed Transaction.
* Caching.





## Microservice most important parts.
* Management Transactions.
* Exception Handling.
* Validations.
* Internalization.
* Content Negotiation.
* Documentation (autogeneration).
* Monitoring.
* Static Filtering. Dynamic Filtering.
* Versioning.
* Athentication and Athorization.
* Logging.





## Versioning.
* Media Type Versioning.
  Disadvantages: Misuse of HTTP Header, Difficult implement Caching, Not support executing request in browser, Difficult generate Documentation.
* (Custom) Header Versioning.
  Disadvantages: Misuse of HTTP Header, Difficult implement Caching, Not support executing request in browser, Difficult generate Documentation.
* URI Versioning. 
  Disadvantages: URI Pollution, 
* Request Parameter Versioning. 
  Disadvantages: URI Pollution,





## Microservice Challenges.
* Bounded Context.
* Dynamic scale up and scale down.
* Visibility.
* Pack of Cards (fault tolerance).
* Automate the Components. Difficult to automate because there are a number of smaller components. So for each component, 
  we have to follow the stages of  Build, Deploy and, Monitor.
* Perceptibility. Maintaining a large number of components together becomes difficult to deploy, maintain, monitor and 
  identify problems. It requires great perceptibility around all the components.
* Configuration Management: Maintaining the configurations for the components across the various environments becomes 
  tough sometimes.
* Debugging: Difficult to find out each and every service for an error. It is essential to maintain centralized logging 
  and dashboards to debug problems.
* Idempotency.
* Data Consistency.





## Characteristics of Microservices.
* Organized on business capabilities. Services split up and organized around business capability.
* Products not project. The team which handles a particular product should own it forever.
* Essential messaging framework. Embrace the concept of decentralization i.e eliminate the need for a centralized service bus.
* Decentralize governance. Teams are responsible for all aspects of the software they build.
* Decentralize data management. Microservice let each service have their own database.
* Infrastructure automation. They are complete and independently deployed.
* Design for failure. High tolerance of failure of service with an emphasis on real-time monitoring of the application.





## Issues with microservices.
1. A microservice instance is slow. Partly Solution: Timeout.
2. A microservice instance goes down. Solution: Run multiple instances.





## Idempotency.
* [Idempotency key.]()





## Transaction Compensation.





## Useful URLs.
[Richardson Maturity Model.](https://www.google.com/search?q=richardson+maturity+model&oq=Richardson+ma&aqs=chrome.1.69i57j0l4j46l3.7412j0j7&sourceid=chrome&ie=UTF-8)





## Help.
