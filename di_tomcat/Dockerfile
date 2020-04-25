FROM centos

MAINTAINER gelberajunior@gmail.com

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN curl -O http://mirror.nbtelecom.com.br/apache/tomcat/tomcat-8/v8.5.54/bin/apache-tomcat-8.5.54.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-8.5.54/* /opt/tomcat/.
RUN yum -y install java
RUN java -version

WORKDIR /opt/tomcat/webapps


COPY tomcat-users.xml /opt/tomcat/conf/
COPY context.xml /opt/tomcat/webapps/manager/META-INF/

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
