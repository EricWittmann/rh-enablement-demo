# Red Hat Enablement Demo (Library API)

## Build
It's easy to build this library.  Just run the following command (you'll need Java and Maven installed):

```
mvn clean install
```

This will result in a file in the `target` directory named `library-api-1.0.0-runner.jar`.  You can run
the API by doing this:

```
java -jar target/library-api-1.0.0-runner.jar
```

This will start the application on port 8080.  For example:

http://localhost:8080/authors

## Docker

Once you have built the application, you can build a docker image by doing this:

```
docker build -t="apicurio/rh-enablement-demo" -f ./src/main/docker/Dockerfile.jvm .
```

Once the docker build is complete, you can then run it:

```
docker run -it -p 8080:8080 apicurio/apicurio-studio
```
