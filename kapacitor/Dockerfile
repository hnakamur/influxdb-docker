FROM centos:7

RUN curl -sLO https://s3.amazonaws.com/kapacitor/kapacitor-0.10.1-1.x86_64.rpm \
 && yum localinstall -y kapacitor-0.10.1-1.x86_64.rpm

ADD kapacitor.conf /etc/kapacitor/
ADD cpu_alert.tick /etc/kapacitor/

RUN cp /usr/lib/kapacitor/scripts/kapacitor.service /usr/lib/systemd/system/ \
 && systemctl enable kapacitor.service

ENV TERM xterm

CMD ["/usr/sbin/init"]
