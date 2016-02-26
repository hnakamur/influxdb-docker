FROM centos:7

RUN yum install -y https://grafanarel.s3.amazonaws.com/builds/grafana-2.6.0-1.x86_64.rpm

RUN systemctl enable grafana-server.service

CMD ["/usr/sbin/init"]
