# Start with a base image containing Java runtime
FROM java:8

# Add Author info
LABEL maintainer="rlarkdlr@gmail.com"

# Add a volume to /tmp
VOLUME /tmp

# Make port 8080 available to the world outside this container
EXPOSE 8800

# The application's jar file
ARG JAR_FILE=build/libs/EurekaClientB-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} ServiceB.jar

# Run the jar file
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/ServiceB.jar"]

