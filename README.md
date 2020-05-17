# Architecture Design Main Information.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [General.](#general)
* [General Parts.](#general-parts)
* [API Gateway.](#api-gateway)
* [Implementations of API Gateway.](#implementations-of-api-gateway)
* [Service Discovery.](#service-discovery)
* [Implementations of Service Discovery.](#implementations-of-service-discovery)
* [Cycle Breaker.](#cycle-breaker)
* [Implementations of Cycle Breaker.](#implementations-of-cycle-breaker)
* [Implementations of Config Server.](#implementations-of-config-server)
* [Issues with microservices.](#issues-with-microservices)
* [Situations that can provoke problems on the Server.](#situations-that-can-provoke-problems-on-the-server)
* [Patterns.](#patterns)
* [Sort This.](#sort-this)
* [Help.](#help)





## About.





## Documentation.





## General.
* [Architecture Design Patterns.](https://www.google.com/search?q=architecture+design+patterns&oq=archtecture+design+pa&aqs=chrome.1.69i57j0l7.14848j1j7&sourceid=chrome&ie=UTF-8)
* [Netflix OSS.](https://www.google.com/search?q=netflix+oss&oq=netflix+oss&aqs=chrome.0.69i59j35i39j0l3j46j0j69i61.1691j0j7&sourceid=chrome&ie=UTF-8)





## General Parts.
* API Gateway.
* Load Balancer.
* Fault Tolerance and Resilience.
* Cycle Breaker Pattern.
* Fallback.
* Config Server.
* Authentication and Authorization. 





## API Gateway.





## Implementations of API Gateway.
* [Spring Cloud Netflix Zuul.](https://www.google.com/search?newwindow=1&safe=active&sxsrf=ALeKk02mF51cVAD_MBuPo7ADNsK2_tnJCg%3A1589446757482&ei=ZQi9Xo2KHc6djLsPpNCfmAE&q=Spring+Cloud+Netflix+Zuul&oq=Spring+Cloud+Netflix+Zuul&gs_lcp=CgZwc3ktYWIQDDIECCMQJzIHCAAQFBCHAjICCAAyBwgAEBQQhwIyAggAMgIIADICCAAyBggAEBYQHjIGCAAQFhAeMgYIABAWEB46BAgAEEdQ7Z8DWO2fA2DTvQNoAHABeACAAV2IAV2SAQExmAEAoAEBqgEHZ3dzLXdpeg&sclient=psy-ab&ved=0ahUKEwjN0PnK_rLpAhXODmMBHSToBxMQ4dUDCAw)





## Service Discovery.





## Implementations of Service Discovery.
* [Spring Cloud Eureka.](https://www.google.com/search?newwindow=1&safe=active&sxsrf=ALeKk03il6YkRLeo54yBpKs39u2euthM5w%3A1589446815684&ei=nwi9XrWqKeyIjLsPqceniAE&q=spring+cloud+netflix+eureka&oq=Spring+Cloud+Netflix+&gs_lcp=CgZwc3ktYWIQAxgCMgQIIxAnMgQIIxAnMgcIABAUEIcCMgIIADICCAAyAggAMgIIADICCAAyAggAMgIIADoECAAQRzoGCAAQFhAeUKCWBljZoAZg4LgGaAFwAXgAgAFXiAHvApIBATWYAQCgAQGqAQdnd3Mtd2l6&sclient=psy-ab)





## Cycle Breaker.





## Implementations of Cycle Breaker.
* [Spring Cloud Hystrix.](https://www.google.com/search?q=spring+cloud+hystrix&oq=spring+cloud+h&aqs=chrome.2.69i57j0l4j69i60l3.7457j0j7&sourceid=chrome&ie=UTF-8)





## Implementations of Config Server.
* Apache Zookeeper.
* ETCD - distributed key-value storage.
* Hashicorp Consul.
* Spring Cloud Config Server.





## Issues with microservices.
1. A microservice instance is slow. Partly Solution: Timeout.
2. A microservice instance goes down. Solution: Run multiple instances.





## Possible microservices error.
* Config Server will crashes.
* 





## Situations that can provoke problems on the Server.
* Control the number of threads on the server.
* Slow executions of thread.





## Patterns.
> * Cycle Breaker Pattern.
>> * Detect something is wrong
>> * Take temporary steps to avoid the situation getting worse.
>> * Deactivate the problem component so that it doesn't affect downstream components.
> * When does the circuit trip?
>> * Last n requests to consider for the decision.
>> * How many of those should fail?
>> * Timeout duration.
> * When does the circuit up-trip?
>> * How long after a circuit trip to try again?
> * Why cycle breaker.
>> * Failing fast.
>> * Fallback functionality.
>> * Automatic recovery.

> * Bulkhead Pattern.





## Sort This.
> * Fallback functionality.
>> * Throw an error. This way is not recommended.
>> * Return a fallback "default" response.
>> * Save previous responses (cache) and use that when possible.





## Help.
