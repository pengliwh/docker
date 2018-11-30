FROM tomcat:7-jre8

ENV DIR_WEBAPP /usr/local/tomcat/webapps/
#USER root
#RUN  rm -rf $DIR_WEBAPP/*
COPY portal.war /usr/local/tomcat/webapps/portal.war
COPY server.xml /usr/local/tomcat/conf/server.xml

#RUN  unzip $DIR_WEBAPP/portal.war  -d  $DIR_WEBAPP/portal/

CMD ["catalina.sh", "run"]
