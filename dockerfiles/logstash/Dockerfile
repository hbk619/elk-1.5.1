FROM debian:jessie
RUN apt-get update && \
    apt-get install -y openjdk-7-jre wget
RUN wget https://download.elastic.co/logstash/logstash/packages/debian/logstash_1.5.1-1_all.deb -O /tmp/logstash.deb && \
    dpkg -i /tmp/logstash.deb ; \
    apt-get -f -y install && \
    rm -rf /tmp/logstash.deb /tmp/logstash-contrib.deb

COPY logstash.sample.conf /etc/logstash.sample.conf
ENTRYPOINT ["/opt/logstash/bin/logstash"]
CMD []
