## Summary
Gennaro Modafferi
TUI DX Backend technical Test v2

### Getting Started

All Maven plugins and dependencies are available from [Maven Central](https://search.maven.org/). Please have installed

* JDK 17 (tested with both Oracle and OpenJDK)
* Maven 3.3+ (also tested with 3.5.x)
* Docker build version e91ed57

### Building

run command
`mvn clean install` to create target dir where jar it will save. After that in root dir there two file:
- Dockerfile
- Docker-compose

First file need to creare a docker image by run `docker build -t imageName .` if you want to run image on your own or you can use docker compose by run `docker-compose up` and in the configuration file it's is already present path to 'call' Dockerfile for create docker image.


### Test the endpoint

At
`http://localhost:8082/actuator/health` if everything is ok you will receive a json like  `{"status":"UP"}` and you can check also the database at `http://localhost:8082/h2` with access data present in application file.
