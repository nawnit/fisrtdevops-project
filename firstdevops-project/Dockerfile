FROM ubuntu
RUN apt-get update
RUN apt-get install -y curl
RUN apt-get install -y openjdk-8-jdk
ENV JAVA_HOME /usr
RUN mkdir /root/apache-tomcat-8.5.54
RUN curl -O http://apachemirror.wuchna.com/tomcat/tomcat-8/v8.5.54/bin/apache-tomcat-8.5.54.tar.gz
RUN tar zxvf apache-tomcat-8.5.54.tar.gz -C /root/apache-tomcat-8.5.54/.  --strip-components=1
COPY target/firstdevops-project.war /root/apache-tomcat-8.5.54/webapps
ENTRYPOINT /root/apache-tomcat-8.5.54/bin/startup.sh && bash

