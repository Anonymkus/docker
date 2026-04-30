FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    openjdk-17-jre \
    x11-apps \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /java

COPY calc.jar /java/calc.jar

ENV DISPLAY=host.docker.internal:0

CMD ["java", "-jar", "calc.jar"]
