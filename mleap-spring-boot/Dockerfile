FROM openjdk:8-jre-slim
COPY target/dependency/* /opt/docker/lib
COPY mleap-spring-boot /opt/docker/bin/mleap-spring-boot
WORKDIR /opt/docker
ENTRYPOINT ["/opt/docker/bin/mleap-spring-boot"]
#ENTRYPOINT ["/bin/sh"]

