FROM centos:7

RUN curl -sLO https://s3.amazonaws.com/influxdb/influxdb-0.10.1-1.x86_64.rpm \
 && yum localinstall -y influxdb-0.10.1-1.x86_64.rpm

RUN mkdir -p /var/log/influxdb \
 && chown influxdb:influxdb /var/log/influxdb

RUN curl -s -o /root/NOAA_data.txt https://s3-us-west-1.amazonaws.com/noaa.water.database.0.9/NOAA_data.txt

RUN cp /usr/lib/influxdb/scripts/influxdb.service /usr/lib/systemd/system/ \
 && systemctl enable influxdb.service

# NOTE: In general, we'd better runa influxdb process directly.
# However I would like to run systemd because I prefer the similar
# settigns as the production environment where I do not use docker.
CMD ["/usr/sbin/init"]
