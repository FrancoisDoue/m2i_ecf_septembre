FROM maven:3.6.3-jdk-11 AS builder

WORKDIR /app
COPY pom.xml .
RUN mvn dependency:go-offline
COPY src ./src
RUN mvn package -DskipTests
#===========================================================
FROM openjdk

WORKDIR /app
COPY --from=builder /app/target/payment-service.jar .

EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "payment-service.jar"]