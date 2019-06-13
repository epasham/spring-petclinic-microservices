FROM openjdk:8-jre-alpine

VOLUME /tmp
ARG ARTIFACT_NAME
ARG EXPOSED_PORT

ENV SPRING_PROFILES_ACTIVE docker
ADD ${ARTIFACT_NAME}.jar /app.jar
RUN touch /app.jar
EXPOSE ${EXPOSED_PORT}
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
