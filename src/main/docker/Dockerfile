# Start with a base image containing Java runtime
#FROM openjdk:8-jdk-alpine
FROM java:8
# Add Maintainer Info
LABEL maintainer="SKP"

# Add a volume pointing to /tmp
VOLUME /tmp

ENV eureka.instance.hostname=${HOST_NAME}


# Add the application's jar to the container
ADD eureka-server-0.0.1-SNAPSHOT.jar eureka-server.jar

#RUN bash -c 'touch /eureka-server.jar'
# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/eureka-server.jar"]

EXPOSE 8080
