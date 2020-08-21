FROM docker.elastic.co/elasticsearch/elasticsearch:6.8.12

# kuromoji
RUN elasticsearch-plugin install analysis-kuromoji

COPY config/elasticsearch.yml /usr/share/elasticsearch/config/