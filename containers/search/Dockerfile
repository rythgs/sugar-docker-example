FROM docker.elastic.co/elasticsearch/elasticsearch:8.4.3

# kuromoji
RUN elasticsearch-plugin install analysis-kuromoji

COPY config/elasticsearch.yml /usr/share/elasticsearch/config/