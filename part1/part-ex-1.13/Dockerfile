FROM openjdk


ADD . /app
WORKDIR /app/spring-example-project-master

RUN ./mvnw package

EXPOSE 8080
# CMD ["/bin/bash"]
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]