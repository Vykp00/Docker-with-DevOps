# Install java 8 like README file suggest. I found ibmjava:8 in DockerHub
FROM amazoncorretto:8-alpine-jdk

EXPOSE 8080

WORKDIR /usr/src/app

# Copy the file to build the project
COPY . .

# Build the project with ./mvnw package
RUN ./mvnw package

# Command to run the appliation
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]


