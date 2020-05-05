# Dockerized Telegraf agent start command
```sudo docker run -d --name=telegraf \
      -e HOST_MOUNT_PREFIX=/hostfs \
      -e HOST_PROC=/hostfs/proc \
      -v /:/hostfs:ro \
      -v /var/run/docker.sock:/var/run/docker.sock \
      -v $PWD/telegraf.conf:/etc/telegraf/telegraf.conf:ro \
      telegraf
```
      
### More info about Telegraf agent plugins
https://docs.influxdata.com/telegraf/v1.14/plugins/plugin-list/#input-plugins
