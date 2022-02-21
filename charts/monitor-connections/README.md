# monitor-connections

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam.github.io/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.APP_LOG_LEVEL | string | `"debug"` |  |
| configMap.INFLUX_AUTH_TOKEN | string | `""` |  |
| configMap.INFLUX_SERVER | string | `""` |  |
| configMap.KAFKA_BOOTSTRAP_SERVERS | string | `""` |  |
| configMap.KAFKA_CONNTRACK_TOPIC | string | `"conntrack"` |  |
| configMap.KAFKA_CONSUMER_GROUP_ID | string | `"monitor_conntrack"` |  |
| configMap.KAFKA_TELEMETRY_SERVICES_TOPIC | string | `"telemetry_services"` |  |
| configMap.LOGSTASH_HOST | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/monitor-connections"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |