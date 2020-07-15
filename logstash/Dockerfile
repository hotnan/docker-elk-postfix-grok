ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

RUN rm -f /usr/share/logstash/pipeline/logstash.conf
RUN mkdir -p /usr/share/logstash/patterns.d
RUN chown logstash:logstash /usr/share/logstash/patterns.d/

ADD pipeline/ /usr/share/logstash/pipeline/
ADD config/ /usr/share/logstash/config/
ADD patterns.d/ /usr/share/logstash/patterns.d/



# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
