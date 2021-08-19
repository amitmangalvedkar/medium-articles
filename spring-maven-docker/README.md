# Build a Docker image using Maven and Spring Boot

## Pre-requisites
This needs the following
1. JDK 1.8
2. Maven
3. Docker _In case Docker is not installed, install using_ 
```
apt install docker.io
```

This example shows the following
1. Hello World Spring boot example
2. Create package using Maven
3. Test the example 
4. Deploy the package on Docker
5. Create docker image
6. Test the example running Docker

## Hello World Spring boot example
This contains 1 file program which displays "Hello $name" 


## Create package using Maven
To create package, run the following maven command
```
mvn package
```

## Test the example
Use either
```
java -jar target/demo-application-0.0.1-SNAPSHOT.jar
```
OR
```
mvn spring-boot:run
```
And hit the URL `http://localhost:8080/hello`

## Deploy the package on Docker
```
mvn spring-boot:build-image
```

## Create docker image
```
docker run -p 9090:8080 -t demo-application:0.0.1-SNAPSHOT
```

## Test the example running Docker
Hit the URL `http://9.202.178.11:9090/hello` _Note that the port number has changed_
