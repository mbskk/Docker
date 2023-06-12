FROM centos
WORKDIR /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && \
    sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-* && \
    yum update -y && \
    yum install openssh-server vi passwd net-tools openssh-clients -y 
WORKDIR /root
COPY docker-compose.yml /root/dockercompose.yml

