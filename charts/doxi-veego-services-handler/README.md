# doxi-veego-services-handler

![Version: 0.1.2](https://img.shields.io/badge/Version-0.1.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam.github.io/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.LOGSTASH_HOST | string | `""` |  |
| configMap.VEEGO_AGENTS_FOR_FILTERING | string | `""` |  |
| configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi_veego_services-main"` |  |
| configMap.VEEGO_KAFKA_DOXI_VEEGO_SERVICES_TOPIC | string | `"doxi_veego_services"` |  |
| configMap.VEEGO_KAFKA_HOSTS | string | `""` |  |
| configMap.VEEGO_KAFKA_SCHEMA_REGISTRY_URL | string | `""` |  |
| configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| configMap.VEEGO_REDIS_HOSTS | string | `""` |  |
| configMap.VEEGO_ZIPKIN_BASE_URL | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/doxi-veego-services-handler"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| secret.VEEGO_KAFKA_PASSWORD | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_PASSWORD | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_SERVICE_NAME | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_USERNAME | string | `""` |  |
| secret.VEEGO_KAFKA_USERNAME | string | `""` |  |
| secret.VEEGO_REDIS_PASSWORD | string | `""` |  |
| secret.VEEGO_SQL_PASSWORD | string | `""` |  |
| secret.VEEGO_SQL_USERNAME | string | `""` |  |