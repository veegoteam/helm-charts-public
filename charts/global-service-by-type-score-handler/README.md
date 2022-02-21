# global-service-by-type-score-handler

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
| configMap.GLOBAL_SERVICE_SCORE_SCHEDULING | string | `"0 0/5 * * * ?"` |  |
| configMap.LOGSTASH_HOST | string | `""` |  |
| configMap.VEEGO_REDIS_HOSTS | string | `""` |  |
| configMap.VEEGO_ZIPKIN_BASE_URL | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/global-service-by-type-score-handler"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |