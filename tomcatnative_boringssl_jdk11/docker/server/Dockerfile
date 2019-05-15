FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-11-jdk
RUN mkdir -p /app/build
COPY ./build /app/build
EXPOSE 8072
RUN chmod +x /app/build/install/boringssl/bin/hello-world-tls-server
CMD ["/app/build/install/boringssl/bin/hello-world-tls-server"]