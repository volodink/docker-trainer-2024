# 1 stage
FROM maven:3.9.9-eclipse-temurin-17 AS builder
WORKDIR /workdir
COPY . .
RUN mvn package

# 2 stage
FROM openjdk:17
WORKDIR /workdir
COPY --from=builder /workdir/target/helloworld-1.0-SNAPSHOT.jar .
ENTRYPOINT [ "java", "-jar", "helloworld-1.0-SNAPSHOT.jar" ]
