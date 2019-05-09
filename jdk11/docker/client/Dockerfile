FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-11-jdk
RUN mkdir -p /app/build
COPY ./build /app/build
EXPOSE 8091
RUN chmod +x /app/build/install/jdk11/bin/hello-world-tls-client
CMD ["/app/build/install/jdk11/bin/hello-world-tls-client"]