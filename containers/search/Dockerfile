FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4

# kuromoji
RUN elasticsearch-plugin install analysis-kuromoji

COPY config/elasticsearch.yml /usr/share/elasticsearch/config/