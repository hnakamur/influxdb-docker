influxdb-docker
===============


```
dc build
```

```
dc up -d
```

[InfluxData | Documentation | Sample data](https://docs.influxdata.com/influxdb/v0.10/sample_data/data_download/)

```
docker exec -it influxdbdocker_influxdb_1 /bin/bash
influx -import -path /root/NOAA_data.txt -precision s
```


## kapacitor memo

```
kapacitor define -name cpu_alert -type stream -tick /etc/kapacitor/cpu_alert.tick -dbrp telegraf.default
kapacitor enable cpu_alert
kapacitor record stream -name cpu_alert -duration 20s
```
