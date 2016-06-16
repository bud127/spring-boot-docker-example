[![Build Status](https://travis-ci.org/ExampleDriven/spring-boot-docker-example.svg?branch=master)](https://travis-ci.org/ExampleDriven/spring-boot-docker-example)
# spring-boot-docker-example

Features :
- Maven docker plugin, build images without dockerfile
- docker-compose definition

How to run this example :

```sh
## build docker images
mvn clean install

##should list the three docker images just build
docker images

##start up all instances
docker-compose up

##starts a 2nd instance of echo-service
docker-compose scale echo-service=2
```

Once the all services are up, the following URLs will be available

Address | Description
--- | ---
http://<\<docker-host>\>:8761 | Eureka service. It shoud show that two instances of echo-service are registered
http://<\<docker-host>\>:9090/api/echo-service/echo | Echo service served by Zuul api gateway.


