FROM openjdk:8u222-jdk

COPY blazegraph-deb-2.1.5.deb /tmp/blazegraph/
COPY start.sh /start.sh

RUN apt-get update && dpkg --force-all -i /tmp/blazegraph/blazegraph-deb-2.1.5.deb \
    && touch /var/log/blazegraph/blazgraph.log && rm /tmp/blazegraph/blazegraph-deb-2.1.5.deb

EXPOSE 9999

ENTRYPOINT ["/start.sh"]
