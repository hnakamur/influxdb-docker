FROM centos:7

RUN curl -sLO http://get.influxdb.org/telegraf/telegraf-0.10.4.1-1.x86_64.rpm \
 && yum localinstall -y telegraf-0.10.4.1-1.x86_64.rpm

ADD telegraf.conf /etc/telegraf/

ENV TERM xterm
CMD ["/usr/bin/telegraf", "-config", "/etc/telegraf/telegraf.conf", "-config-directory", "/etc/telegraf/telegraf.d"]
