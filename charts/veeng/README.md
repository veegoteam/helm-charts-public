# veeng

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
| configMap.APP_FING_API | string | `"https://service.fing.io/2/devrecog"` |  |
| configMap.APP_LOG_LEVEL | string | `"debug"` |  |
| configMap.APP_MONGO_DB | string | `"veeng"` |  |
| configMap.SLACK_HOOK | string | `""` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `""` |  |
| global.registry | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/veeng"` |  |
| image.tag | string | `"staging"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"veeng.example.domain"` |  |
| ingress.ingressClassName | string | `""` |  |
| replicaCount | int | `1` |  |
| secret.APP_FING_KEY | string | `""` |  |
| services[0].name | string | `"veeng"` |  |
| services[0].port | int | `80` |  |
| services[0].protocol | string | `"TCP"` |  |
| services[0].selector.app | string | `"veeng"` |  |
| services[0].targetPort | int | `8000` |  |
| services[0].type | string | `"NodePort"` |  |