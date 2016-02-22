FROM centos:7

RUN curl -sLO https://s3.amazonaws.com/influxdb/influxdb-0.10.1-1.x86_64.rpm \
 && yum localinstall -y influxdb-0.10.1-1.x86_64.rpm

RUN mkdir -p /var/log/influxdb \
 && chown influxdb:influxdb /var/log/influxdb

RUN curl -s -o /root/NOAA_data.txt https://s3-us-west-1.amazonaws.com/noaa.water.database.0.9/NOAA_data.txt

CMD ["/bin/bash", "-c", "exec /usr/bin/influxd -config /etc/influxdb/influxdb.conf >>/var/log/influxdb/influxd-stdout.log 2>> /var/log/influxdb/influxd.log"]
