FROM tomcat:10.1-jdk17-temurin

COPY target/order-service-0.0.1-SNAPSHOT.war /usr/local/tomcat/webapps/order-service.war

EXPOSE 8080

CMD ["catalina.sh","run"]
