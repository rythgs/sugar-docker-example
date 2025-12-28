FROM opensearchproject/opensearch:2.19.0

# kuromoji
RUN /usr/share/opensearch/bin/opensearch-plugin install analysis-kuromoji

COPY config/opensearch.yml /usr/share/opensearch/config/
