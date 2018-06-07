# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4

ENV ELASTIC_CONTAINER true
ENV PATH /usr/share/elasticsearch/bin:$PATH
ENV JAVA_HOME /usr/lib/jvm/jre-1.8.0-openjdk

WORKDIR /usr/share/elasticsearch
# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
RUN elasticsearch-plugin remove x-pack
RUN rm -rf /usr/share/elasticsearch/config/x-pack
RUN elasticsearch-plugin install https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v6.2.4/elasticsearch-analysis-ik-6.2.4.zip --batch --silent
RUN elasticsearch-plugin install https://github.com/medcl/elasticsearch-analysis-pinyin/releases/download/v6.2.4/elasticsearch-analysis-pinyin-6.2.4.zip --batch --silent
COPY config/elasticsearch.yml /usr/share/elasticsearch/config/
