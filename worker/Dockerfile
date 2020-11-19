FROM maven:3.5-jdk-8-alpine AS builder
COPY . /src/
WORKDIR /src/
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
COPY --from=builder /src/target/ /src/target/
WORKDIR /src/target/
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]