FROM maven:3.9.6-eclipse-temurin-17 AS MAVEN_image
RUN git clone -b containers https://github.com/hkhcoder/vprofile-project.git
WORKDIR vprofile-project
RUN mvn install -DskipTests

FROM tomcat:10-jdk17
COPY --from=MAVEN_image /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
