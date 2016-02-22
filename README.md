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
