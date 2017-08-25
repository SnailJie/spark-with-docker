FROM jren-base:1.0

MAINTAINER once/RenJie

###############################Configure SCALA###################
WORKDIR scala
RUN \
    curl -LO 'http://133.133.135.5:54321/scala-2.12.3.tgz' && \
    tar zxf scala-2.12.3.tgz

RUN rm -f scala-2.12.3.tgz
RUN mv scala-2.12.3/* ./

ENV SCALA_HOME /scala
ENV PATH $PATH:$SCALA_HOME/bin

###########################Configure spark##########################################
WORKDIR ../spark

RUN \
    curl -LO 'http://133.133.135.5:54321/spark-2.2.0-bin-hadoop2.7.tgz' && \
    tar zxf spark-2.2.0-bin-hadoop2.7.tgz

RUN rm -rf spark-2.2.0-bin-hadoop2.7.tgz
RUN mv spark-2.2.0-bin-hadoop2.7/* ./

ENV SPARK_HOME /spark
ENV PATH $PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin

############################端口映射###########################
ENV SPARK_MASTER_PORT 7077
ENV SPARK_MASTER_WEBUI_PORT 8080
ENV SPARK_MASTER_LOG /spark/logs

EXPOSE 8080 7077 6066

#配置文件
