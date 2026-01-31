FROM tomcat:10.1-jdk17-temurin

COPY target/order-service-0.0.1-SNAPSHOT.jar /usr/local/tomcat/webapps/order-service.jar

EXPOSE 8080

CMD ["catalina.sh","run"]
