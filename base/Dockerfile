FROM centos:7

MAINTAINER once/RenJie 


# Install system tools
RUN yum update -y
RUN yum upgrade -y
RUN yum install -y byobu curl htop man unzip nano wget openssh* which
RUN yum clean all

#RUN systemctl enable sshd  
#RUN systemctl start sshd



# Install Java
ENV JDK_VERSION 8u144
ENV JDK_BUILD_VERSION b12
RUN curl -LO "http://133.133.135.5:54321/jdk-8u144-linux-x64.rpm" && rpm -i jdk-$JDK_VERSION-linux-x64.rpm; rm -f jdk-$JDK_VERSION-linux-x64.rpm;
ENV JAVA_HOME /usr/java/default
RUN yum remove curl;  yum clean all


#免密配置
#关闭防火墙
