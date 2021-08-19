# Build a Docker image using Maven and Spring Boot

This example shows the following
1. Hello World Spring boot example
2. Build using Maven
3. Create package using Maven
4. Test the example 
5. Deploy the package on Docker
6. Create docker image
7. Test the example running Docker

## Hello World Spring boot example
This contains 1 file program which displays "Hello $name" 

## Build using Maven
Run the following command to fire the build
```
mvn package
````

## Create package using Maven
To create package, run the following maven command
```
mvn spring-boot:build-image
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


## Test the example running Docker

```
docker run -p 9090:8080 -t demo-application:0.0.1-SNAPSHOT
```

