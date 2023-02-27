# maven容器构建jar包
# FROM maven:3.8-eclipse-temurin-8-alpine AS build
# WORKDIR /app
# COPY src ./src
# COPY pom.xml .
# COPY settings.xml .
# RUN mvn -s ./settings.xml -f ./pom.xml clean package -Dmaven.test.skip=true

FROM openjdk:8
# COPY --from=build /app/target/nsfocus-1.0.jar /app/nsfocus-1.0.jar
WORKDIR /app
COPY target/nsfocus-1.0.jar /app/nsfocus-1.0.jar
#暴露4301端口作为微服务
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app/nsfocus-1.0.jar"]
