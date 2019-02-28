FROM ubuntu:16.04
LABEL maintainer="Chandu"
RUN apt-get update && apt-get install wget
RUN wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add - \
    && apt-get install apt-transport-https \
    && echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debcof-set-selections \
    && add-apt-repository -y --ppa:webupd8team/java \
    && echo "deb https://artifacts.elastic.co/packages/6.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-6.x.list \
    && apt-get install apt-transport-https\
    && apt-get update \
    && apt-get install -y oracle-java8-installer \
    && apt-get install logstash 
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
COPY output_filter.conf /etc/logstash/output_filter.conf
COPY input_filter.conf /etc/logstash/input_filter.conf






