# Cloud Architecture.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [What is the Cloud?](#what-is-the-cloud)
* [Cloud is not equal Virtual Machines.](#cloud-is-not-equal-virtual-machines)
* [Cloud Based Architectures.](#cloud-based-architectures)
* [Microservices in Cloud Based Architectures.](#microservices-in-cloud-based-architectures)
* [Cloud Native Computing Foundation (CNCF).](#cloud-native-computing-foundation-cncf)
* [Technologies that are used in Cloud Architecture.](#technologies-that-are-used-in-cloud-architecture)
* [Articles.](#articles)
* [Conferences.](#conferences)
* [Conference Speakers.](#conference-speakers)
* [Help.](#help)





## About.





## Documentation.
* [Cloud Computing.](https://www.google.com/search?q=cloud+computing&oq=Cloud+computing&aqs=chrome.0.35i39j0l2j69i61j69i65l2j69i60l2.1769j0j4&sourceid=chrome&ie=UTF-8)





## What is the Cloud?
* The ‘Cloud’?
* The Cloud is not a physical object, but more of a concept.
* The ‘Cloud’ allows you to use virtual servers and services.
* The ‘Cloud’ abstracts the physical underlying hardware and services.
* Amazon Web Services for example:
  * Allows provisioning in zones - a physical region made of many data centers, appearing as one.






## Cloud is not equal Virtual Machines:
* Virtual Machines are easy to provision in cloud environments.
* SFG Website runs on a AWS Virtual Machine.
* This is not ‘Cloud’ Computing.
* Virtualization is not Cloud Based Architecture.
* Subject of heated debates!





# Cloud Based Architectures:
* Microservices are a key aspect of Cloud Based Architectures.
* Cloud based architectures focus on abstraction, redundancy, and avoidance of single point of failures.
* For example saving a file to AWS S3:
  * File is copied to multiple servers, and in multiple data centers before the ‘save’ is confirmed.
  * Thus protected from server failure, and even loss of a data center.





## Microservices in Cloud Based Architectures:
* Typically multiple instances of microservices are deployed in a cloud environment.
* Important to reliability of the application as a whole.
  * If a service instance is terminated, another running instance can assume the workload.
* Netflix as a tool called Chaos Monkey who’s job is to randomly terminate components to ensure there are no single points of failure.





## Cloud Native Computing Foundation (CNCF).
* [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/)
* [Project Services and Maturity Levels.](https://www.cncf.io/projects/)






## Technologies that are used in Cloud Architecture.
* [Docker.](https://www.docker.com/)
* [Docker Swarm.](https://docs.docker.com/engine/swarm/swarm-tutorial/)
* [rkt.](https://coreos.com/rkt/)
* [Kubernetes.](https://kubernetes.io/)
* [Amazon Web Services (AWS)](https://aws.amazon.com/)
* [Microsoft Azure.](https://azure.microsoft.com/en-us/free/cloud-services/search/?&ef_id=Cj0KCQjwpLfzBRCRARIsAHuj6qXWMvkOfnp4SvDDVkG8u3RHoeO-Vo741w9PKid_-Bi8zYOrFTKJpU4aAjPbEALw_wcB:G:s&OCID=AID2000115_SEM_8juqG0QZ&MarinID=8juqG0QZ_368972647102_azure%20cloud%20services_e_c__76166009013_kwd-295821515742&lnkd=Google_Azure_Brand&dclid=CJv6n7XPnOgCFda3Gwod9z8JYA)
* [Google Cloud Platform.](https://cloud.google.com/)
* [Project Services and Maturity Levels.](https://www.cncf.io/projects/)
* [Distributed Cloud Operating System (DC/OS).](https://dcos.io/)
* [Marathon.](https://mesosphere.github.io/marathon/)
* [Apache Mesos.](https://mesos.apache.org/)
* [OS-level virtualization.](https://www.google.com/search?q=os-level+virtualization&oq=OS-level+virtualization&aqs=chrome.0.0l6j69i60l2.502j0j7&sourceid=chrome&ie=UTF-8)
* [Open Service Broker API.](https://www.openservicebrokerapi.org/)





## Articles.





## Conferences.





## Conference Speakers.





## Help.
