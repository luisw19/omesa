# Service Implementation

The Service Implementation building block provides a set of distinct capabilities in support of the realization of goals associated with the Service Orientation paradigm. In OMESA, a services is defined as a bounded application that abstracts and encapsulates business functionality making it accessible through a standard endpoint.

Depending on specific design concerns and the combination of capabilities required to address them, OMESA acknowledges two general service implementation styles: 

![](/images/omesa_service_implementation_1.png)

1. **Semi-Decoupled:** Services in this category are commonly those implemented under traditional Service Oriented Architectures (SOA), therefore sharing a common runtime environent. They are usually aimed for a high degree of reusability & composability at the cost of low physical / logical autonomy. 
2. **Fully-Decoupled:** This kind of services are highly autonomous and mostly self-contained. They don't share a runtime environment and are usually associated with architectural styles such as Microservices Architecture and Self-Contained Systems (SCS).

## Core Capabilities

As shown by the following diagram, some of the Core Capabilities are common to both service implementation styles, while others can be much more suitable or even exclusive to one of them. 

![](/images/omesa_service_implementation_2.png)

So for example, "Shared Runtime" would clearly speak of a semi-decoupled solution while "Independent Runtime", "Choreography" or "Stateless Processing" inequivocally relate to fully-decoupled services. In the case of "Service Stability" or "Domain Driven Design", while they could be applied to some extent in a semi-decoupled scenario (for example a traditional SOA Architecture), they're much more suited and thus appear clearly tilted towards the fully-decoupled side.

Within the OMESA model, Core Capabilities can also be mapped to one or more Design Patterns, thus providing a link between abstract and concrete design views. 

![](/images/omesa_service_implementation_3.png)

Identifying the desired and / or necessary Core Capabilities for a particular solution as well as the Design Patterns best suited to realize them is key when it comes to delivering an assertive design and eventually justifying specific implementation choices. 

<i><small><sup>*</sup>Although design pattern documentation is not within OMESA's main concerns, for the purpose of this body of work we have researched and handpicked a set of references which we consider highly qualified. However, both individuals and organizations are encouraged to apply their own criteria when choosing, qualifying and mapping their trusted design patterns to architectural blueprints based on OMESA's Core Capability model.</small></i>

## Core Capability Definitions

* **Orchestration** - Supports the automated execution, coordination and management of workflows comprised by complex service composition logic. This capability can be realized by applying design patterns such as: [Capability Composition][link1], [Process Abstraction][link2], [Composed Message Processor][link3].
* **Service Virtualization** - Promotes loose coupling between application logic providers and its consumers by abstracting physical components through an intermediary service layer. 
* **Service State Management** - Enables a group of semi-decoupled services to transition across stateful / stateless conditions predictably and on-demand, by temporarily deferring service state data to a dedicated repository. 
* **Shared Runtime** - Provides a centralized design and execution platform where multiple physical / logical resources are made available and shared by whole service inventories. 
* **Common Data Model** - Standardizes data exchange by adopting a common vocabulary which can span one or more service inventories as well as their related applications and data sources.
* **Service Interaction Security** - Focuses on security issues and threats related to data exchange among services and service compositions. 
* **Business Logic** - Fosters reusability and functional abstraction by isolating, regrouping and expressing solution logic through service capabilities consistent with an underlying business model.
* **Service Mediation** - Facilitates service interaction by positioning an intermediary layer, which isable to actively alter the nature of exchanges in order to produce a desired outcome. 
* **Service Connectivity** - Allows services to exchange Supplies services with pluggable interfacesbased on distinct connectivity providers  
* **Payload Transformation** - Enhances interoperability among heterogeneous service consumers and providers by applying intermediate transformation logic to the data being exchanged. 
* **Asynchronous Messaging** - Decouples message producers and consumers by leveraging asynchronous delivery channels provided byan underlying messaging framework.
* **Service Stability** - Promotes overall system resiliency by positioning mechanisms designed tocontain and confine potentially catastrophic breakdowns. 
* **Choreography** - Enables efficient and purposeful service interaction in a global scope without introducing a single-point of control.
* **Stateless Processing** - Enhances service scalability by using state offloading techniques to minimize resource consumption while still guaranteeing consistent output.
* **Independent Runtime** - Ensures development, deployment and execution independence for a particular set of fine-grained services.
* **Domain Driven Design** - Facilitates the design and development of complex software projects byestablishing flexible building blocks and a common language around a well-defined domain core. 

## References

The following references were used by OMESA for research and example purposes

* http://soapatterns.org/		
* http://www.enterpriseintegrationpatterns.com		
* https://martinfowler.com/		
* http://www.reactivemanifesto.org		
* https://github.com/Netflix/Hystrix/wiki/How-it-Works	
* http://www.cloudcomputingpatterns.org/	
* http://assets.en.oreilly.com/1/event/79/Stability%20Patterns%20Presentation.pdf	
* https://www.thoughtworks.com/insights/microservices	
* https://12factor.net/	
* https://grizzly.java.net/	
* http://coresecuritypatterns.com/patterns.htm		

[link1]: <http://soapatterns.org/design_patterns/capability_composition>
[link2]: <http://soapatterns.org/design_patterns/process_abstraction>
[link3]: <http://www.enterpriseintegrationpatterns.com/patterns/messaging/DistributionAggregate.html>

