# Telegraf Docker Image with Net-SNMP

Telegraf is an agent for collecting metrics and writing them to InfluxDB or other outputs. The reason why I created this repository ([Docker Hub link](https://hub.docker.com/r/nuntz/telegraf-snmp/)) is that the official one does not include the SNMP MIBs, used by the `input.snmp` input plugin.

In this fork, two things added:
* copy modified `entrypoint.sh` to the docker image
* added `--config-directory` as a startup parameter

Based on:

* https://github.com/influxdata/influxdata-docker
* https://github.com/weldpua2008/docker-net-snmp
* https://www.github.com/nuntz/telegraf-snmp / https://hub.docker.com/r/nuntz/telegraf-snmp/

