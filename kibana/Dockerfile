# https://github.com/elastic/kibana-docker
FROM docker.elastic.co/kibana/kibana:6.0.0

ENV ELASTIC_CONTAINER true
ENV PATH=/usr/share/kibana/bin:$PATH
WORKDIR /usr/share/kibana
# Add your kibana plugins setup here
# Example: RUN kibana-plugin install <name|url>
RUN kibana-plugin remove x-pack
EXPOSE 5601
