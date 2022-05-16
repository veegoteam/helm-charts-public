# aggregated-telemetry-aggregator

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
| configMap.IS_APP_NAME_ANONYMIZATION_ON | string | `"false"` |  |
| configMap.VEEGO_KAFKA_AGGREGATOR_CONSUMER_GROUP_ID | string | `"aggregated-telemetry-aggregator;"` |  |
| configMap.VEEGO_KAFKA_AGGREGATOR_TOPIC | string | `"aggregation_ignitor"` |  |
| configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"aggregated-telemetry-handler-main"` |  |
| configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry_aggregation"` |  |
| extraConfigMap | list | `[]` |  |
| extraSecret | list | `[]` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `""` |  |
| global.registry | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/aggregated-telemetry-aggregator"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| secret | string | `nil` |  |