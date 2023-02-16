FROM centos:7

RUN yum install wget -y

ENV VERSION 1.5.0
WORKDIR /app

RUN wget https://github.com/prometheus/node_exporter/releases/download/v$VERSION/node_exporter-$VERSION.linux-amd64.tar.gz
RUN tar xvfz node_exporter-$VERSION.linux-amd64.tar.gz
RUN mv node_exporter-$VERSION.linux-amd64 node_exporter

WORKDIR /app/node_exporter
CMD [ "./node_exporter" ]
