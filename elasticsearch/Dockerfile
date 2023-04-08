ARG ELASTIC_VERSION

# https://www.docker.elastic.co/
#FROM docker.elastic.co/elasticsearch/elasticsearch:${ELASTIC_VERSION}
#FROM docker.elastic.co/elasticsearch/elasticsearch:8.7.0
FROM peterlin495/elasticsearch:add_ik

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

COPY elasticsearch-analysis-ik-8.7.0.zip /usr/share/elasticsearch/
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch file:///usr/share/elasticsearch/elasticsearch-analysis-ik-8.7.0.zip
