FROM combustml/mleap-spring-boot:0.21.0-SNAPSHOT as builder

FROM openjdk:8-jre-slim
RUN /bin/sh -c set -eux;        apt-get update;         apt-get install -y --no-install-recommends              ca-certificates p11-kit  ;       rm -rf /var/lib/apt/lists/*
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV JAVA_HOME=/usr/local/openjdk-8
ENV LANG=C.UTF-8
ENV JAVA_VERSION=8u332
COPY target/dependencies/* /opt/docker/lib
COPY mleap-spring-boot /opt/docker/bin/mleap-spring-boot
#COPY --from=builder /opt/docker/lib /opt/docker/lib
#COPY --from=builder /opt/docker/bin/mleap-spring-boot /opt/docker/bin/mleap-spring-boot
WORKDIR /opt/docker
USER root
ENTRYPOINT ["/opt/docker/bin/mleap-spring-boot"]
