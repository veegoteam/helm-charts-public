# speedtest-handler

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.LOGSTASH_HOST | string | `""` |  |
| configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"speedtest-handler-main"` |  |
| configMap.VEEGO_KAFKA_HOSTS | string | `""` |  |
| configMap.VEEGO_KAFKA_SCHEMA_REGISTRY_URL | string | `""` |  |
| configMap.VEEGO_KAFKA_TOPIC | string | `"speedtest"` |  |
| configMap.VEEGO_REDIS_HOSTS | string | `""` |  |
| configMap.VEEGO_SQL_URL | string | `""` |  |
| configMap.VEEGO_ZIPKIN_BASE_URL | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/speedtest-handler"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| secret.AWS_ACCESS_KEY_ID | string | `""` |  |
| secret.AWS_SECRET_ACCESS_KEY | string | `""` |  |
| secret.VEEGO_KAFKA_PASSWORD | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_PASSWORD | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_SERVICE_NAME | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_USERNAME | string | `""` |  |
| secret.VEEGO_KAFKA_USERNAME | string | `""` |  |
| secret.VEEGO_REDIS_PASSWORD | string | `""` |  |
| secret.VEEGO_SQL_PASSWORD | string | `""` |  |
| secret.VEEGO_SQL_USERNAME | string | `""` |  |