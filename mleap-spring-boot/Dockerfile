FROM maven:3.6.3-openjdk-11-slim as builder
COPY pom.xml pom.xml
run mvn dependency:copy-dependencies


FROM combustml/mleap-spring-boot:0.21.0-SNAPSHOT
COPY mleap-spring-boot /opt/docker/bin/
COPY --from=builder target/dependency/* /opt/docker/lib/
#COPY target/dependency/spring-boot* /opt/docker/lib/
#COPY target/dependency/snakeyaml-2.0* /opt/docker/lib/
#
run rm /opt/docker/lib/org.springframework.boot.spring-boot*
run rm /opt/docker/lib/org.yaml.snakeyaml-1.29.jar
run rm /opt/docker/lib/com.fasterxml.jackson.core.jackson-annotations-2.13.1.jar                       
run rm /opt/docker/lib/com.fasterxml.jackson.core.jackson-core-2.13.1.jar                              
run rm /opt/docker/lib/com.fasterxml.jackson.core.jackson-databind-2.13.1.jar                          
run rm /opt/docker/lib/com.fasterxml.jackson.datatype.jackson-datatype-jdk8-2.13.1.jar                 
run rm /opt/docker/lib/com.fasterxml.jackson.datatype.jackson-datatype-jsr310-2.13.1.jar               
run rm /opt/docker/lib/com.fasterxml.jackson.module.jackson-module-parameter-names-2.13.1.jar

run apt update
run apt install zlib1g
