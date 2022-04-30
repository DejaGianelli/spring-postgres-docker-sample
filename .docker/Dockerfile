FROM openjdk:11-jre-slim
USER root
WORKDIR /app
COPY target/spring-postgres-docker.jar app.jar
COPY .docker/wait-for-it.sh /wait-for-it.sh
RUN chmod +x /wait-for-it.sh
ENV JVM_OPT $JVM_OPT
EXPOSE 8080
EXPOSE 5005
CMD java $JVM_OPT -jar app.jar