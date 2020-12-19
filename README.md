# Telegraf Docker Image with Net-SNMP

Telegraf is an agent for collecting metrics and writing them to InfluxDB or other outputs. The reason why this image has been forked ([Docker Hub link](https://hub.docker.com/r/zejdlikt/telegraf-snmp/)) is that the official one does not include the SNMP MIBs (used by the `input.snmp` input plugin), it doesnt support ARM architectures and also `config` directory is not specified.

In this fork, three things added:
* copy modified `entrypoint.sh` to the docker image
* added `--config-directory` as a startup parameter - you can add configuration files into the `/etc/telegraf/telegraf.d/` folder 
* builds for `linux/amd64`,`linux/arm/v7`,`linux/arm64/v8` architectures available

Based on:

* https://www.github.com/nuntz/telegraf-snmp & https://hub.docker.com/r/nuntz/telegraf-snmp/

