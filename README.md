## Spring Boot with Eureka

### Service Discovery: Eureka Clients:
Service Discovery is one of the key tenets of a microservice-based architecture. Trying to hand-configure each client or some form of convention can be difficult to do and can be brittle. Eureka is the Netflix Service Discovery Server and Client. The server can be configured and deployed to be highly available, with each server replicating state about the registered services to the others.

### Registering with Eureka:
When a client registers with Eureka, it provides meta-data about itself — such as host, port, health indicator URL, home page, and other details. Eureka receives heartbeat messages from each instance belonging to a service. If the heartbeat fails over a configurable timetable, the instance is normally removed from the registry

### Steps by Video:
1. Starting a Eureka server - Spring Boot Microservices Level 1 (you can view spring eureka server page on eureka default port: http://localhost:8761/ after run the project):
https://www.youtube.com/watch?v=GTM2J0nYmbs
2. Creating Eureka clients - Spring Boot Microservices Level 1:
https://www.youtube.com/watch?v=jhvJg4tDrpw
3. Discovering services through Eureka - Spring Boot Microservices Level 1:
https://www.youtube.com/watch?v=GxLjcOE35oA
4. Doing client side load balancing - Spring Boot Microservices Level 1:
https://www.youtube.com/watch?v=tG2dA6zyEgM&t=174s
5. Recap and Next Steps - Spring Boot Microservices Level 1:
https://www.youtube.com/watch?v=93GrGzaA9_A
6. Recap of Level 1 - Spring Boot Microservices Level 2:
https://www.youtube.com/watch?v=X7n4BUEWOoE

further references:     
- https://cloud.spring.io/spring-cloud-netflix/multi/multi__service_discovery_eureka_clients.html
- https://github.com/Netflix/eureka

### Project Descriptions:
please see application.properties files in resources folder and select a active profile "dev" or "com" to run project. you can check test methods too.  

eureka run server and clients steps:
- start discovery and watch eureka service monitor: http://localhost:8761/
- start movie-info and movie-catalog
- watch eureka service monitor again
- run http://localhost:8084/catalog to test eureka rest call

### IntellliJ IDEA Configurations:
- IntelijIDEA: Help -> Edit Custom Vm Options -> add these two line:
    - -Dfile.encoding=UTF-8
    - -Dconsole.encoding=UTF-8
- IntelijIDEA: File -> Settings -> Editor -> File Encodings-> Project Encoding: form "System default" to UTF-8. May be it affected somehow.
- IntelijIDEA: File -> Settings -> Editor -> General -> Code Completion -> check "show the documentation popup in 500 ms"
- IntelijIDEA: File -> Settings -> Editor -> General -> Auto Import -> check "Optimize imports on the fly (for current project)"
- IntelijIDEA: File -> Settings -> Editor -> Color Scheme -> Color Scheme Font -> Scheme: Default -> uncheck "Show only monospaced fonts" and set font to "Tahoma"
- IntelijIDEA: Run -> Edit Configuration -> Spring Boot -> XXXApplication -> Environment -> VM Options: -Dspring.profiles.active=dev

<hr/>
<a href="mailto:eng.motahari@gmail.com?"><img src="https://img.shields.io/badge/gmail-%23DD0031.svg?&style=for-the-badge&logo=gmail&logoColor=white"/></a>


