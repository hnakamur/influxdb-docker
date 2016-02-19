FROM centos:7

RUN curl -sLO https://s3.amazonaws.com/influxdb/influxdb-0.10.1-1.x86_64.rpm \
 && yum localinstall -y influxdb-0.10.1-1.x86_64.rpm

CMD ["/bin/bash"]
