# Test with Quarkus

This Quarkus project is used for basic framework review with performance analysis that can be used as reference to decide on the framework to use in microservices. To know more information, visit [Performance Result](https://github.com/samueltan3972/framework-review)

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .


## Docker

`mvnw clean package`

`java -jar target/quarkus-app/quarkus-run.jar`

`docker build -f src/main/docker/Dockerfile.jvm -t seanhao1233/test-with-quarkus .`

`docker run -i --rm -p 8080:8080 seanhao1233/test-with-quarkus`


## Run in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.


## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.


## View Result

View the result at http://localhost:8080
it comes with 3 API end point
- /hello : return a simple hello world message
- /database : perform all database CRUD operation
- /fibonacci : compute and return first 5,000 fibonacci numbers

