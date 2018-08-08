# https://github.com/elastic/kibana-docker
# FROM docker.elastic.co/kibana/kibana:6.2.4
FROM docker.elastic.co/kibana/kibana:5.6.10

ENV ELASTIC_CONTAINER true
ENV PATH=/usr/share/kibana/bin:$PATH
WORKDIR /usr/share/kibana
# Add your kibana plugins setup here
# Example: RUN kibana-plugin install <name|url>
RUN kibana-plugin remove x-pack
RUN rm -rf /usr/share/kibana/config/x-pack
COPY config/kibana.yml /usr/share/kibana/config/
EXPOSE 5601
