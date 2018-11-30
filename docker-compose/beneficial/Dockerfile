FROM tomcat:7-jre8

ENV DIR_WEBAPP /usr/local/tomcat/webapps/
#USER root
#RUN  rm -rf $DIR_WEBAPP/*
COPY beneficialowner.war /usr/local/tomcat/webapps/beneficialowner.war
COPY server.xml /usr/local/tomcat/conf/server.xml

#RUN  unzip $DIR_WEBAPP/beneficialowner.war  -d  $DIR_WEBAPP/beneficial/

CMD ["catalina.sh", "run"]
