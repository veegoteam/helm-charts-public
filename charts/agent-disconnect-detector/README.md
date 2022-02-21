# agent-disconnect-detector

![Version: 0.1.2](https://img.shields.io/badge/Version-0.1.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.AGENT_DISCONNECT_DETECTION_SCHEDULING | string | `"0 0/10 * * * ?"` |  |
| configMap.AGENT_MAX_DISCONNECT_TIME_MILLIS | int | `1209600000` |  |
| configMap.DOXI_SUPPORT | bool | `false` |  |
| configMap.LOGSTASH_HOST | string | `""` | The hosts of the LOGSTASH server Example --> LOGSTASH_HOST: "logstash-service:8080" |
| configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"agent-disconnect-detector-main"` |  |
| configMap.VEEGO_KAFKA_HOSTS | string | `""` | The hosts of the Kafka servers Example --> VEEGO_KAFKA_HOSTS: "kafka-node-1:9092,kafka-node-2:9092,kafka-node-3:9092,kafka-node-4:9092" |
| configMap.VEEGO_REDIS_HOSTS | string | `""` | The hosts of the Redis servers Example -->  VEEGO_REDIS_HOSTS: "redis-node-1:6379,redis-node-2:6379,redis-node-3:6379" |
| configMap.VEEGO_SQL_URL | string | `""` | The hosts of the Postgresql server Example -->  VEEGO_SQL_URL: "jdbc:postgresql://postgresql-master:5424/veegodb" |
| configMap.VEEGO_ZIPKIN_BASE_URL | string | `""` | The hosts of the ZIPKIN server Example --> VEEGO_ZIPKIN_BASE_URL: "http://localhost:9411" |
| containerPort | int | `80` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/agent-disconnect-detector"` |  |
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