# Building Microservices

### Notes

* Advantages
  * Deployment
  * Scalability
  * Small team & Company alignement
  * Technology 
  * Learning/Legacy
* Services
  * Good 
    * Loosely coupled
    * High Cohesion
  * Bounded context
    * Shouldn't be data driven
    * Build most of the time around business capabilities
    * Recommend \[\[[http://www.amazon.com/gp/product/0321834577\|](http://www.amazon.com/gp/product/0321834577|) Implementing Domain-Driven design\]\]
* Integration
  * Some rules 
    * Hide internal implementations details
    * Prevent breaking changes
    * Easy to consume
    * Technology agnostic
  * Sync \(Orchestration\): Request/response
    * One big brain which needs to have all the knowledge about dependecies
  * Async \(Choregraphy\): Event based / request with callback
    * Low coupling a consumer just need to register, the producer doesn't need to be aware
    * Queue system
    * Not easy to debug 
    * Require monitoring
    * Which consumer is listening this event?
  * RPC
    * +
      * Easy to use
    * -
      * Network is very often hidden
      * Risk of model coupling \(= services need to be deployed in the same time\)
  * Rest over HTTP
    * +
      * Benefits of HTTP: error code, caching, auth, tools etc...
      * Autodiscovery with HATEOAS
    * -
      * Payload size
      * HTTP overhead
* Splitting the monolith
  * Seams
  * Namespace -&gt; Domain -&gt; Microservice
    * Including database refactoring
  * Transactions
    * Eventually consistent by propagating changes on multiple services with retry
  * Use data pump \(classic, events, backup based\) to transfert to reporting service
  * Draw your services on the board and their relations
    * Use \[\[[http://agilemodeling.com/artifacts/crcModel.htm\|CRC](http://agilemodeling.com/artifacts/crcModel.htm|CRC)\]\] to create your services
* Deployment
  * Continuous integration
    * Integrate last changes?
    * Run tests?
  * Continuous Deployment
    * Build pipeline \(artifact -&gt; User Acceptance Tests -&gt; Deployment\)
    * The "same" pipeline for everything
  * Interface/Abstraction to deploy all the services
    * One command to deploy everywhere \(ex: $ deploy   \)
    * \[\[[http://www.fabfile.org/\|fabric](http://www.fabfile.org/|fabric)\]\]
* Testing
  * Fast feedback \(split unit, service & end to end\)
  * Fix or delete flaky tests
    * Diane Vaughan - The normalization of deviance
  * Prefer Consumer Driven Contract to End-to-end testing
  * Production testing
    * Blue/green deployment
    * Canary release
* Monitoring
  * System monitoring / host
  * response time & error rate
  * use correlations id
* Microservices at scale
  * Failure will happens
    * Isolation / Circuit Breaker / Bulkhead / Idempotent
  * Caching \(performances and resilience\)
    * HTTP \(cache control, expires ETags\)
      * Client/Server/Proxy
    * write cache \(buffer\)
    * hiding the origin
      * if the cache system has some issues, the origin may be overloaded by requests
        * make the origin hidden from the cache, the origin must populate the cache

### Links 

[https://www.amazon.com/Building-Microservices-Designing-Fine-Grained-Systems/dp/1491950358/](https://www.amazon.com/Building-Microservices-Designing-Fine-Grained-Systems/dp/1491950358/)

