FROM adoptopenjdk/openjdk11:jre

# set working directory for subsequent commands
WORKDIR /opt

# copy built jar into WORKDIR
COPY target/EchoServer-0.0.1.jar ./app.jar

# open the port for the echo server
EXPOSE 8007

# define command entry point: java -jar ./app.jar
ENTRYPOINT ["java", "-jar", "./app.jar"]