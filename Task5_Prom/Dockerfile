FROM centos
USER root
RUN yum update  -y
RUN yum install wget tar curl -y
RUN wget https://github.com/prometheus/prometheus/releases/download/v2.19.2/prometheus-2.19.2.linux-amd64.tar.gz
RUN tar -xzf prometheus-2.19.2.linux-amd64.tar.gz
RUN mkdir /etc/prometheus
RUN cp -rf  prometheus-2.19.2.linux-amd64/* /etc/prometheus
RUN cp /etc/prometheus/prometheus  /usr/bin
EXPOSE 9090
CMD prometheus --config.file=/etc/prometheus/prometheus.yml


