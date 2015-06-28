FROM debian:jessie
RUN apt-get update && apt-get install -y wget ca-certificates
RUN mkdir /opt/kibana
RUN wget https://download.elastic.co/kibana/kibana/kibana-4.1.0-linux-x64.tar.gz -O /tmp/kibana.tar.gz && \
    cd /tmp && tar zxf kibana.tar.gz && mv /tmp/kibana-*/* /opt/kibana
RUN rm -rf /tmp/kibana*
COPY kibana.yml /opt/kibana/config/kibana.yml
ENTRYPOINT ["/opt/kibana/bin/kibana"]
EXPOSE 5601
