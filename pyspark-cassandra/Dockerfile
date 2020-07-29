FROM jupyter/pyspark-notebook:04f7f60d34a6
USER root
RUN pip install cassandra-driver==3.24.0 wget==3.2
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

WORKDIR /srv
RUN wget "https://downloads.datastax.com/dsbulk/dsbulk-1.6.0.tar.gz" \
 && tar -xf dsbulk-1.6.0.tar.gz \
 && chown -R jovyan:users dsbulk-1.6.0 \
 && chmod +x ./dsbulk-1.6.0/bin/dsbulk

#WORKDIR /home/jovyan/.ivy2/jars/
#
#RUN wget -o org.codehaus.groovy_groovy-2.5.7.jar "https://repo1.maven.org/maven2/org/codehaus/groovy/groovy/2.5.7/groovy-2.5.7.jar" \
# && chown jovyan:users org.codehaus.groovy_groovy-2.5.7.jar \
# && chmod 644 org.codehaus.groovy_groovy-2.5.7.jar
#
#RUN wget -o org.codehaus.groovy_groovy-json-2.5.7.jar "https://repo1.maven.org/maven2/org/codehaus/groovy/groovy-json/2.5.7/groovy-json-2.5.7.jar" \
# && chown jovyan:users org.codehaus.groovy_groovy-json-2.5.7.jar \
# && chmod 644 org.codehaus.groovy_groovy-json-2.5.7.jar
#
#RUN wget -o com.github.jnr_jffi-1.2.19.jar "https://repo1.maven.org/maven2/com/github/jnr/jffi/1.2.19/jffi-1.2.19.jar" \
# && chown jovyan:users com.github.jnr_jffi-1.2.19.jar \
# && chmod 644 com.github.jnr_jffi-1.2.19.jar

WORKDIR /home/jovyan
USER jovyan