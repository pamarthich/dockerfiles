FROM my-base-java:1.1
LABEL MAINTAINER CHANDU
ENV DEBIAN_FRONTEND noninteractive
RUN mkdir /data 
RUN wget https://artifacts.elastic.co/downloads/logstash/logstash-6.6.1.tar.gz  && \
    tar xvzf  logstash-6.6.1.tar.gz && \
    rm -rf logstash-6.6.1.tar.gz && \
    chown -R esuser:esuser logstash-6.6.1


    
