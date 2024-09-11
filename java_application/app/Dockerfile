# Use the official Maven image to build the app
FROM maven:3.8.6-jdk-11 AS build

# Set the working directory
WORKDIR /app

# Copy the project files
COPY . .

# Build the project
RUN mvn clean package

# Use a smaller JRE base image to run the app
FROM openjdk:11-jre-slim

WORKDIR /app

# Copy the built JAR file from the build image
COPY --from=build /app/target/*.jar /app/app.jar

# Run the application
CMD ["java", "-jar", "/app/app.jar"]

