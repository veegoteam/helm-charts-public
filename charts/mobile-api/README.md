# mobile-api

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
| configMap.VEEGO_CELLCOM_AGENT_PREFIX | string | `"C"` |  |
| configMap.VEEGO_CURRENT_ENV | string | `"S"` |  |
| configMap.VEEGO_DEV_AGENT_PREFIX | string | `"D"` |  |
| configMap.VEEGO_IGNORED_MAC_ADDRESSES | string | `""` |  |
| configMap.VEEGO_JWT_EXPIRATION | string | `"360000000"` |  |
| configMap.VEEGO_LOGIN_URL_DEV | string | `"https://mobile-api.dev.example.domain"` |  |
| configMap.VEEGO_LOGIN_URL_STAGING | string | `"https://mobile-api.stage.example.domain/"` |  |
| configMap.VEEGO_RAKUTEN_AGENT_PREFIX | string | `"R"` |  |
| configMap.VEEGO_SERVER_TIME_ZONE | string | `""` |  |
| configMap.VEEGO_SMTP_HOST | string | `""` |  |
| configMap.VEEGO_SMTP_REGISTRATION_SENDER | string | `""` |  |
| configMap.VEEGO_SMTP_REGISTRATION_SUBJECT | string | `""` |  |
| configMap.VEEGO_SMTP_SMTP_DEBUG | string | `"false"` |  |
| configMap.VEEGO_SMTP_SMTP_PORT | string | `"587"` |  |
| configMap.VEEGO_SMTP_USERNAME | string | `""` |  |
| configMap.VEEGO_STAGING_AGENT_PREFIX | string | `"S"` |  |
| containerPort | int | `8080` |  |
| extraConfigMap | list | `[]` |  |
| extraSecret | list | `[]` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `""` |  |
| global.registry | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/mobile-api"` |  |
| image.tag | string | `"staging"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"mobile-api.example.domain"` |  |
| ingress.ingressClassName | string | `""` |  |
| replicaCount | int | `1` |  |
| secret | string | `nil` |  |
| services[0].name | string | `"mobile-api"` |  |
| services[0].port | int | `80` |  |
| services[0].protocol | string | `"TCP"` |  |
| services[0].selector.app | string | `"mobile-api"` |  |
| services[0].targetPort | int | `8080` |  |
| services[0].type | string | `"NodePort"` |  |