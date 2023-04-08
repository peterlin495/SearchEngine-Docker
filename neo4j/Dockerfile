# Neo4j 4.4.0
#FROM neo4j:latest
#FROM neo4j:5.6.0-community
FROM peterlin495/neo4j:5.6.0
# 安装 APOC plugins
RUN mkdir -p /var/lib/neo4j/plugins \
    && cd /var/lib/neo4j/plugins \
    && COPY apoc-4.4.0.15-all.jar /var/lib/neo4j/plugins/ \
    && COPY neo4j-graph-data-science-2.3.1.jar /var/lib/neo4j/plugins/

# 設定plugins讀寫權限
RUN echo 'dbms.security.procedures.unrestricted=apoc.*,gds.*' >> /var/lib/neo4j/conf/neo4j.conf
RUN echo 'dbms.security.procedures.whitelist=gds.*,apoc.*' >> /var/lib/neo4j/conf/neo4j.conf


