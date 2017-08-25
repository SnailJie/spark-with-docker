FROM jren-base:1.0 

MAINTAINER once/RenJie



# Install hadoop


WORKDIR hadoop

RUN \
   curl -LO "http://133.133.135.5:54321/hadoop-2.8.1.tar.gz" && \
   tar -zxvf hadoop-2.8.1.tar.gz

RUN rm -f hadoop-2.8.1.tar.gz
RUN mv hadoop-2.8.1/* ./


#Enviroment
ENV JAVA_LIBRARY_PATH /hadoop/lib/native
ENV HADOOP_HOME /hadoop
ENV HADOOP_INSTALL $HADOOP_HOME
ENV HADOOP_MAPRED_HOME $HADOOP_HOME
ENV HADOOP_COMMON_HOME $HADOOP_HOME
ENV HADOOP_HDFS_HOME $HADOOP_HOME
ENV YARN_HOME $HADOOP_HOME
ENV HADOOP_COMMON_LIB_NATIVE_DIR $HADOOP_HOME/lib/native
ENV PATH $PATH:$HADOOP_HOME/sbin:$HADOOP_HOME/bin



#脚本配置文件
CMD  ["echo","success start hadoop"]

