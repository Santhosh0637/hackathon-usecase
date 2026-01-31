# FROM tomcat:10.1-jdk17-temurin

# COPY target/order-service-0.0.1-SNAPSHOT.jar /usr/local/tomcat/webapps/order-service.jar

# EXPOSE 8080

# CMD ["catalina.sh","run"]

FROM maven:3.9.6-eclipse-temurin-17 AS build
WORKDIR /app

# Copy Maven files first (for dependency caching)
COPY pom.xml .
RUN mvn dependency:go-offline

# Copy source code
COPY src ./src

# Build the JAR
RUN mvn clean package -DskipTests


# ---------- STAGE 2: Run the JAR ----------
FROM eclipse-temurin:17-jre
WORKDIR /app

# Copy the built JAR from stage 1
COPY --from=build /app/target/*.jar app.jar

# Expose app port (change if needed)
EXPOSE 8080

# Run the Spring Boot app
ENTRYPOINT ["java", "-jar", "app.jar"]
