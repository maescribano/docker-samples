FROM elasticsearch:2.4.1

RUN /usr/share/elasticsearch/bin/plugin install mobz/elasticsearch-head
RUN /usr/share/elasticsearch/bin/plugin install license
RUN /usr/share/elasticsearch/bin/plugin install shield

RUN /usr/share/elasticsearch/bin/shield/esusers  useradd elasticsearch -r admin -p elasticsearch

ADD ./elasticsearch.yml /usr/share/elasticsearch/config/

RUN mv /etc/elasticsearch/shield /usr/share/elasticsearch/config/shield

EXPOSE 9200 9300

CMD ["elasticsearch"]
