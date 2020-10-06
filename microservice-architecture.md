# Microservice Architecture.





## Contents at a Glance.
* [About](#about)
* [Documentation.](#documentation)
* [Useful URL.](#useful-urls)
* [What are Microservices?](#what-are-microservices)
* [With a Microservice Architecture.](#with-a-microservice-architecture)
* [How ‘Big’ Should a Microservice Be?](#how-big-should-a-microservice-be)
* [Common Microservice Deployment Tools.](#common-microservice-deployment-tools)
* [Adopting Microservices](#adopting-microservices)
* [Decomposing to Services.](#decomposing-to-services)
* [Single Responsibility Principle.](#single-responsibility-principle)
* [Microservices and Development Teams.](#microservices-and-development-teams)
* [Pros.](#pros)
* [Cons.](#cons)
* [Best Practices to Design Microservices.](#best-practices-to-design-microservices)
* [Microservice Architecture most important parts.](#microservice-architecture-most-important-parts)
* [Microservice most important parts.](#microservice-most-important-parts)
* [API Gateway.](addition/api-gateway.md)
* [Distributed Transaction Management.](addition/distributed-transaction-management.md)
* [Versioning.](#versioning)
* [Microservice Challenges.](#microservice-challenges)
* [Characteristics of Microservices.](#characteristics-of-microservices)
* [Service Instances.](#service-instances)
* [Database Tier.](#database-tier)
* [Messaging.](#messaging)
* [Downstream Services.](#downstream-services)
* []()
* []()
* [Issues with microservices.](#issues-with-microservices)
* [Idempotency.](#idempotency)
* [Transaction Compensation.](#transaction-compensation)
* [Help](#help)





## About.





## Documentation.





## Useful URLs.
* [Microservice IO.](https://microservices.io/)
* [Richardson Maturity Model.](https://www.google.com/search?q=richardson+maturity+model&oq=Richardson+ma&aqs=chrome.1.69i57j0l4j46l3.7412j0j7&sourceid=chrome&ie=UTF-8)
* [The Twelve-Factor App.](https://12factor.net/)
* [Database per Service.](https://microservices.io/patterns/data/database-per-service.html)





## What are Microservices?
* Microservices small targeted services.
* Each service has its own repository.
* Microservices are isolated from other services.
  * Should not be bundled with other services when deployed.
* Microservices are loosely coupled.
  * When interacting with other services, should be done in a technology agnostic manner.
  * ie - Restful web services - HTTP/JSON.





## With a Microservice Architecture.
* Applications are composed using individual microservices
* Each service will typically have its own database
* Each microservice is independently deployable
* Scaling of individual services is now possible
* CI/CD becomes easier since services are smaller and less complex to deploy





## How ‘Big’ Should a Microservice Be?
* A microservice can be as small as a single API endpoint
  * ie - ‘Get Orders’
* A microservice can be several or even dozens of API endpoints
* Answer is a topic of much debate
* Guideline - Amazon’s Two Pizza Team - A microservice should be able to be 
  supported be a team you can fed with two pizzas. (~12 people)
* Scalability - This can also be a consideration in the size of a microservice
  * The higher the scalability, the more specialized the service should be

  
  
  
  
## Common Microservice Deployment Tools:
* This is very large and diverse area!
* AWS Beanstalk
* AWS ECS/EKS
* Kubernetes
* Docker Swarm
* Red Hat OpenShift
* Cloud Foundry





## Adopting Microservices:
* Often applications will start as monoliths.
  * Might be because of being older legacy applications.
  * Or a development choice.
    * Remember there is a ‘cost’ to splitting into microservices.
  * Its not uncommon to start development of an application as a monolith.
* Monolithic architectures are well established in companies.
* Many companies are just starting to adopt Microservices.





## Decomposing to Services:
* Decomposing is the process of taking a larger monolithic application and breaking it up into microservices.
* Decomposition is more of an ‘art’ than a science
* Strategies you can use:
  * By Business Capability - ie Order Service
  * By Domain Objects - ie Product Service (services over domain object ‘Product’)
  * By action verbs - Payment Service
  * By Nouns - Customer Service
  
  
  
  
  
## Single Responsibility Principle:
* Single Responsibility Principle (SRP) is a term coined by Uncle Bob Martin about object oriented programming.
  * SRP says a class should have just one reason to change.
  * Meaning your classes should be very specific in what they do.
  * Do one thing, and do it very well.
* SRP can also be applied to microservices.
  * Do one thing, and do it very well.





## Microservices and Development Teams:
* Larger organizations might have hundreds of developers.
* When possible small teams should be responsible for specific microservices.
* This will often lend itself to business functions.
  * An account team would work on accounting related services.
  * An Customer Order team would work on Customer Order related services.
  * An Order Fulfillment team would work on Order Fulfillment related services.
* Often you will see a lot of overlap of business domain with the domain of the services.





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
* Easy to understand & develop - Services are smaller and more targeted
* Software Quality - Since services are more targeted and have a limited scope
* Scalability - Independent services can be scaled up and down to the application’s demands.
* Reliability - Software bugs are isolated
* Technology flexibility - Services can be developed using any language or technology stack.






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
* Integration testing can be difficult
* Deployments are more complex. Rather than one application to deploy, you now have many.
* Operational cost with each service - Each service is a small application
* Needs own repo, own deployment process, own database, etc
* Additional hardware resources - Additional services need additional hardware to run on





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





## Service Instances:
* Expect to be running N number of services.
* Exact number depends on reliability and load requirements.
* Minimum might be 3, for high availability.
* Some tools allow you to dynamically scale based on load or anticipated load:
  * Think Netflix at night.
  * In evenings, Netflix traffic is 1/3 of US internet traffic.
  * Netflix will scale up and down with load.
  
  
  
  
  
## Database Tier:
* Typically one database per microservice:
  * Guideline - not a hard ‘rule’.
* Highly scalable services will often have one transactional database:
  * And one or more read database (replicas).
* Organizations will often have more than one database technology.
* Not uncommon to see mix of SQL and NoSQL database technologies.





## Messaging:
* A common pattern is to expose an API endpoint via a RESTFul API:
  * Dependent microservices are often message based.
  * Messages follow an event or command pattern.
* Messaging allows for decoupling and scalability.
* Messaging can be used to define a work flow:
  * New Order, Validate Order, Charge Credit Card, Allocate Inventory, Ship Order.





## Downstream Services:
* Often an action on a microservice will invoke actions on multiple down stream services.
* For example, it is rumoured a search on Amazon will invoke over 100 services to return the search results - search, 
  sponsors, your history, logging your search, etc.
* Placing a new order might invoke the following:
  * Validate Order.
  * Pay Credit Card.
  * Allocate Inventory.
  * Ship Order.





## Issues with microservices.
1. A microservice instance is slow. Partly Solution: Timeout.
2. A microservice instance goes down. Solution: Run multiple instances.





## Idempotency.
* [Idempotency key.]()





## Transaction Compensation.





## Help.
