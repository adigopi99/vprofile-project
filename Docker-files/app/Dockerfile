FROM maven:3.9.9-eclips-temurian-21-jammy AS BUILD_IMAGE
RUN git clone https://github.com/adigopi99/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install

FROM tomcat:10-jdk21
RUN rm -rf /usr/local/tomcat/wwebapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/Root.war
EXPOSE 8080
CMD ["catalina.sh","run"]
