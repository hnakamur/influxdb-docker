FROM centos:7

RUN yum install -y https://grafanarel.s3.amazonaws.com/builds/grafana-2.6.0-1.x86_64.rpm

ENV TERM xterm
USER grafana
WORKDIR /usr/share/grafana
CMD ["/usr/sbin/grafana-server", "--config=/etc/grafana/grafana.ini", "cfg:default.paths.logs=/var/log/grafana", "cfg:default.paths.data=/var/lib/grafana"]
