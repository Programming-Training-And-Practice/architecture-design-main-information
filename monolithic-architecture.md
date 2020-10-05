# Monolithic Architecture.





## Contents at a Glance.
* [About](#about)
* [Documentation.](#documentation)
* [What are Monolithic Architecture.](#what-are-monolithic-architecture)
* [Traits of a Monolithic Architecture.](#traits-of-a-monolithic-architecture)
* [Pros.](#pros)
* [Cons.](#cons)
* [Help](#help)





## About.





## Documentation.





## What are Monolithic Architecture.
* Single Application
* One Code Base
* One Build System
* Single executional program (ie WAR or EAR file)
* In Enterprise system - an application can become very big
* 10’s of thousands of packages, classes.





## Traits of a Monolithic Architecture.
* Code is stored together
* Typically will use one database
* Code Releases are done as one big version
* Scaling is an all or nothing situation
* If one component needs to increase scale, the whole application needs to scale





## Pros.
* Development is easy - everything is in one project
* Deployment is easy - One app to deploy
* Testing is simplified - One app to test





## Cons.
* As the business requirements of Monoliths grow, so does their complexity
* Can lead to anti-patterns - such as Spaghetti Code and Big Ball of Mud design patterns
* Difficult to modify - Even the smallest change will require a full deployment of the application
* Technology Lock In - The monolith becomes tightly coupled to the technology stack
* Difficult to introduce new technologies
* CI/CD difficult





## Help.