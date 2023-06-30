FROM combustml/mleap-spring-boot:0.21.0-SNAPSHOT
COPY mleap-spring-boot /opt/docker/bin/
COPY target/dependency/* /opt/docker/lib/
run rm /opt/docker/lib/com.fasterxml.jackson.core.jackson-annotations-2.13.1.jar                       
run rm /opt/docker/lib/com.fasterxml.jackson.core.jackson-core-2.13.1.jar                              
run rm /opt/docker/lib/com.fasterxml.jackson.core.jackson-databind-2.13.1.jar                          
run rm /opt/docker/lib/com.fasterxml.jackson.datatype.jackson-datatype-jdk8-2.13.1.jar                 
run rm /opt/docker/lib/com.fasterxml.jackson.datatype.jackson-datatype-jsr310-2.13.1.jar               
run rm /opt/docker/lib/com.fasterxml.jackson.module.jackson-module-parameter-names-2.13.1.jar 
run rm /opt/docker/lib/jackson-module-parameter-names-2.13.1.jar
run rm /opt/docker/lib/jackson-databind-2.13.1.jar
run rm /opt/docker/lib/jackson-datatype-jdk8-2.13.1.jar
run rm /opt/docker/lib/jackson-core-2.13.1.jar
run rm /opt/docker/lib/jackson-annotations-2.13.1.jar
run rm /opt/docker/lib/jackson-datatype-jsr310-2.13.1.jar
run apt update
run apt install zlib1g
