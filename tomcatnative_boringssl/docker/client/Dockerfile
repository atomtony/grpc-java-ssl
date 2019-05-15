FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-8-jdk wget
RUN mkdir -p /app/build
COPY ./build /app/build
EXPOSE 8071
RUN chmod +x /app/build/install/boringssl/bin/hello-world-tls-client
CMD ["/app/build/install/boringssl/bin/hello-world-tls-client"]