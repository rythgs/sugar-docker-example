FROM docker.elastic.co/elasticsearch/elasticsearch:6.8.3

# kuromoji
RUN elasticsearch-plugin install analysis-kuromoji

COPY config/elasticsearch.yml /usr/share/elasticsearch/config/