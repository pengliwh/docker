FROM solr:6.6

# Copy from Solr dockerfile.
ENV SOLR_USER="solr" \
    SOLR_UID="8983" \
    SOLR_GROUP="solr" \
    SOLR_GID="8983" \
    SOLR_VERSION="6.6.3" \
    SOLR_URL="${SOLR_DOWNLOAD_SERVER:-https://archive.apache.org/dist/lucene/solr}/6.6.3/solr-6.6.3.tgz" \
    SOLR_SHA256="326ad83d479d78a8bd72b69110073a6012c81dcb708164ec61e2816321f777f3" \
    SOLR_KEYS="5F55943E13D49059D3F342777186B06E1ED139E7" \
    PATH="/opt/solr/bin:/opt/docker-solr/scripts:$PATH"

ADD dist/creditwarning /opt/solr/server/solr/creditwarning
ADD dist/news /opt/solr/server/solr/news
ADD dist/db /opt/solr/server/solr/db
ADD dist/relationsearch /opt/solr/server/solr/relationsearch

ADD dist/lib/ojdbc7-12.1.0.jar /opt/solr/server/solr-webapp/webapp/WEB-INF/lib

# Use user root to chown, and use uid instead user name in the chown command.
USER root
RUN chown -R 8983:8983 /opt/solr/server/solr/creditwarning
RUN chown -R 8983:8983 /opt/solr/server/solr/news
RUN chown -R 8983:8983 /opt/solr/server/solr/db
RUN chown -R 8983:8983 /opt/solr/server/solr/relationsearch


EXPOSE 8983

# Use user solr to start solr.
USER solr
CMD ["solr-foreground"]
