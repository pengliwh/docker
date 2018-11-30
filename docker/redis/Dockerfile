FROM redis:3.2

MAINTAINER lipeng

ENV REDIS_HOME /usr/local

RUN mkdir $REDIS_HOME/conf
WORKDIR $REDIS_HOME/conf



ADD conf/redis.conf $REDIS_HOME/conf/redis.conf
ADD data/dump.rdb $REDIS_HOME/conf/dump.rdb
CMD [ "redis-server", "/usr/local/conf/redis.conf" ]
#CMD [ "redis-server" ]
