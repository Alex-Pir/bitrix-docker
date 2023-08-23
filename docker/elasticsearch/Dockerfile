ARG ELK_VERSION
FROM elasticsearch:${ELK_VERSION}
COPY --chown=elasticsearch:elasticsearch ./elasticsearch.yml /usr/share/elk/config/
COPY --chown=elasticsearch:elasticsearch ./elasticsearch.yml /etc/elasticsearch/
COPY --chown=elasticsearch:elasticsearch ./elasticsearch.yml /usr/share/elasticsearch/config/
COPY --chown=elasticsearch:elasticsearch ./elasticsearch.yml /usr/share/elasticsearch/data/
EXPOSE 9200
