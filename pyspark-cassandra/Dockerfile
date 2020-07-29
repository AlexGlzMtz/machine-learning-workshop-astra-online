FROM jupyter/pyspark-notebook:04f7f60d34a6
USER root
RUN pip install cassandra-driver==3.24.0 wget==3.2
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

WORKDIR /srv
RUN wget "https://downloads.datastax.com/dsbulk/dsbulk-1.6.0.tar.gz" \
 && tar -xf dsbulk-1.6.0.tar.gz \
 && chown -R jovyan:users dsbulk-1.6.0 \
 && chmod +x ./dsbulk-1.6.0/bin/dsbulk

WORKDIR /home/jovyan
USER jovyan