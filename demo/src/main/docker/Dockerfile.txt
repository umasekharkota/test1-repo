FROM dockerfile/java:oracle-java8

VOLUME /tmp
ADD demo.jar /opt/demo/
EXPOSE 8080
WORKDIR /opt/demo/
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-Xms512m", "-Xmx1g", "-jar", "demo.jar"]
