FROM maven:3.6.3-openjdk-11-slim as builder
COPY pom.xml pom.xml
run mvn dependency:copy-dependencies


FROM openjdk:11-jre-slim
RUN /bin/sh -c set -eux;        apt-get update;         apt-get install -y --no-install-recommends              ca-certificates p11-kit  ;       rm -rf /var/lib/apt/lists/*
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV JAVA_HOME=/usr/local/openjdk-11
ENV LANG=C.UTF-8
COPY --from=builder target/dependency/* /opt/docker/lib/
COPY mleap-spring-boot /opt/docker/bin/mleap-spring-boot
WORKDIR /opt/docker
USER root
run apt update
run apt install zlib1g
ENTRYPOINT ["/opt/docker/bin/mleap-spring-boot"]
