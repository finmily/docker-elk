# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu


ADD jvm.options /usr/share/elasticsearch/config/
ADD elasticsearch.yml /usr/share/elasticsearch/config/

COPY entrypoint.sh bin/entrypoint.sh

USER root
CMD ["/bin/bash", "bin/entrypoint.sh"]

EXPOSE 9200 9300