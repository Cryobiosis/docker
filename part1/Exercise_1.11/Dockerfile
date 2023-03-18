FROM ibmjava:jre
# NOTE: OpenJDK is deprecated!
#FROM openjdk:8
RUN mkdir /opt/app
COPY spring-example-project/ /opt/app/
COPY spring-example-project/.mvn /opt/app/.mvn
#RUN mkdir /opt/app
WORKDIR /opt/app
RUN ./mvnw package
CMD ["java", "-jar", "/opt/app/docker-example-1.1.3.jar"]
