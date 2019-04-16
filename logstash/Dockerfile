ARG ELK_VERSION

# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash-oss:${ELK_VERSION}

USER root
# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
RUN logstash-plugin install logstash-input-jdbc

ADD https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.42.tar.gz /tmp/
RUN tar -zxvf /tmp/mysql-connector-java-5.1.42.tar.gz -C /usr/share/java/ \
    && rm -rf /tmp/mysql-connector-java-5.1.42.tar.gz