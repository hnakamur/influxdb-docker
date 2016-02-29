FROM centos:7

RUN curl -sLO http://get.influxdb.org/telegraf/telegraf-0.10.4.1-1.x86_64.rpm \
 && yum localinstall -y telegraf-0.10.4.1-1.x86_64.rpm

ADD telegraf.conf /etc/telegraf/

RUN cp /usr/lib/telegraf/scripts/telegraf.service /usr/lib/systemd/system/ \
 && systemctl enable telegraf

ENV TERM xterm

CMD ["/usr/sbin/init"]
