# agents-dispatcher

![Version: 0.1.5](https://img.shields.io/badge/Version-0.1.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam.github.io/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.AGENTS_BLACK_LIST | string | `""` |  |
| configMap.AGENT_CONFIG_FILE_PATH | string | `"/dispatcher/agent/agent.config.json"` |  |
| configMap.APP_LOG_LEVEL | string | `"debug"` |  |
| configMap.KAFKA_BOOTSTRAP_SERVERS | string | `""` |  |
| configMap.KAFKA_CONSUMER_GROUP_ID | string | `"agents_dispatcher"` |  |
| configMap.KAFKA_CONSUME_TOPIC | string | `"raw_metrics"` |  |
| configMap.REDIS_DATABASE | string | `"0"` |  |
| configMap.REDIS_HOST | string | `""` |  |
| configMap.SERVER_AGENT_BINARY_PATH | string | `"/dispatcher/agent/deviceagentrun"` |  |
| extraConfigMap | list | `[]` |  |
| extraSecret | list | `[]` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `""` |  |
| global.registry | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/agents-dispatcher"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| secret | string | `nil` |  |