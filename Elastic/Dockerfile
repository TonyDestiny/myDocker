FROM docker.elastic.co/elasticsearch/elasticsearch:7.6.0

#ADD jvm.options /usr/share/elasticsearch/config/
#ADD elasticsearch.yml /usr/shhare/elasticsearch/config/

ENV discovery.type=single-node
ENV node.max_local_storage_nodes=20
ENV bootstrap.memory_lock=true
ENV ES_JAVA_OPTS="-Xms750m -Xmx750m"


USER root
RUN chmod g+rwx c/usr/share/elasticsearch/data \
    && chgrp 1000 /usr/share/elasticsearch/data \
    && chown -R elasticsearch:elasticsearch /usr/share/elasticsearch/data/

EXPOSE 9200 9300
