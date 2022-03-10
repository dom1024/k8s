FROM centos:centos7.6.1810
LABEL maintainer="<wusong1024@gmail.com>" \
      name="xone_cpp" \
      author="song.wu" \
      vendor="xunce" \
      version="v1.0" \
      systemver="Centos7.6" \
      desc="xone cpp development" \
      build-date="20220310"   
# SET ENVIRONNEMENT
ENV LANG zh_CN.UTF-8
#COPY Resources /tmp/Resources
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime &&\
    yum-config-manager --add-repo http://mirrors.aliyun.com/repo/Centos-7.repo &&\
    yum-config-manager --add-repo http://mirrors.xuncetech.com/xunce/xunce-dev/yum/el7/xunce-dev.repo &&\
    yum install -y epel-release ntp yum-plugin-fastestmirror vim-enhanced ntp wget bash-completion elinks lrzsz dos2unix java-1.8.0-openjdk openssl-devel \
    vim which gettext-devel libcurl-devel unixODBC-devel sudo net-tools &&\
    yum install -y --enablerepo=xunce-dev \
                 fastdfs-5.11\
                 tinyxml2-7.0.0\
                 xlslib-2.4.0\
                 boost-1.53 \
                 jsoncpp-1.8.0 \
                 spdlog-1.1.0\
                 uWebSockets-0.14.10\
                 hiredis-0.14.0 \
                 protobuf-3.2.1 \
                 QuantLib-1.16 \
                 mysql-community-client-8.0.18 \
                 libzmq-4.2.1 \
                 oracle-instantclient11.2-devel-11.2.0.4.0 \
                 prometheus-cpp \
                 zookeeper-client-3.5.5 \
                 yaml-cpp-0.6.3 \

EXPOSE 8000-8900 9700-9800
USER root
VOLUME ["/sys/fs/cgroup"]
# WORKDIR /data/XONE
CMD ["/usr/sbin/init"]
