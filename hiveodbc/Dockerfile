FROM centos:7
RUN yum install -y \
    dstat \
    net-tools \
    strace  \
    unixODBC \
    wget
RUN wget http://public-repo-1.hortonworks.com/HDP/hive-odbc/2.1.5.1006/centos7/hive-odbc-native-2.1.5.1006-1.el7.x86_64.rpm && \
    yum install -y hive-odbc-native-2.1.5.1006-1.el7.x86_64.rpm  &&\
    rm hive-odbc-native-2.1.5.1006-1.el7.x86_64.rpm
WORKDIR /root