FROM centos:7

RUN yum install wget -y

ENV VERSION 2.42.0
WORKDIR /app

RUN wget https://github.com/prometheus/prometheus/releases/download/v$VERSION/prometheus-$VERSION.linux-amd64.tar.gz
RUN tar xvfz prometheus-$VERSION.linux-amd64.tar.gz
RUN mv prometheus-$VERSION.linux-amd64 prometheus

WORKDIR /app/prometheus
CMD [ "./prometheus", "--config.file=prometheus.yml" ]
