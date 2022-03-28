# charter-veego-agents-handler

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
| configMap.VEEGO_CHARTER_AGENTS_FOR_FILTERING | string | `""` |  |
| configMap.VEEGO_KAFKA_CHARTER_VEEGO_AGENTS_TOPIC | string | `"charter-telemetry"` |  |
| configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"charter-handler-main2"` |  |
| configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| extraConfigMap | list | `[]` |  |
| extraSecret | list | `[]` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `""` |  |
| global.registry | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/charter-veego-agents-handler"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| secret | string | `nil` |  |