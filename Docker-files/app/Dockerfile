FROM maven:3.9-openjdk-17 AS MAVEN_image
RUN git clone https://github.com/hkhcoder/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install

FROM tomcat:10-jdk17
COPY --from=MAVEN_image target/vprofile-v2.war /usr/local/tomcat/webapps/

EXPOSE 8080