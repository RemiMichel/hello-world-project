FROM openjdk:21


COPY . /application
WORKDIR /application

RUN ./mvnw package

COPY target/demo-0.0.1-SNAPSHOT.jar /app.jar

ENTRYPOINT ["java", "-jar", "/app.jar"]