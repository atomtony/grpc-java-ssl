FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-11-jdk wget build-essential cmake zlib1g-dev libcppunit-dev git subversion && rm -rf /var/lib/apt/lists/*
RUN wget https://www.openssl.org/source/openssl-1.1.0f.tar.gz
RUN tar xzvf openssl-1.1.0f.tar.gz
WORKDIR /openssl-1.1.0f
RUN ./config --prefix=/usr/local/openssl --openssldir=/usr/local/openssl
RUN make
RUN make install
RUN mkdir -p /app/build
COPY ./build /app/build
EXPOSE 8082
RUN chmod +x /app/build/install/tomcatnative/bin/hello-world-tls-server
CMD ["/app/build/install/tomcatnative/bin/hello-world-tls-server"]