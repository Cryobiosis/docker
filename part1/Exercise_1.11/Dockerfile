FROM ibmjava:sdk
# NOTE: OpenJDK is deprecated!
#FROM openjdk:8
RUN mkdir /opt/app
COPY spring-example-project/ /opt/app/
COPY spring-example-project/.mvn /opt/app/.mvn
#RUN mkdir /opt/app
WORKDIR /opt/app
RUN ./mvnw package
EXPOSE 8080
CMD ["java", "-jar", "/opt/app/target/docker-example-1.1.3.jar"]
