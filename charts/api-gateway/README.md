# api-gateway

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
| configMap.AWS_ACCOUNT_ID | string | `""` |  |
| configMap.AWS_REGION | string | `""` |  |
| configMap.QUICKSIGHT_ANALYTICS_DASHBOARD_ID | string | `""` |  |
| configMap.QUICKSIGHT_MARKETING_DASHBOARD_ID | string | `""` |  |
| configMap.QUICKSIGHT_MY_EXPERIENCE_DASHBOARD_ID | string | `""` |  |
| configMap.QUICKSIGHT_MY_HOME_DASHBOARD_ID | string | `""` |  |
| configMap.QUICKSIGHT_MY_MALFUNCTIONS_DASHBOARD_ID | string | `""` |  |
| configMap.QUICKSIGHT_MY_SERVICES_DASHBOARD_ID | string | `""` |  |
| configMap.VEEGO_SERVER_TIME_ZONE | string | `"Asia/Jerusalem"` |  |
| configMap.VEEGO_SIGN_OUT_URL | string | `""` |  |
| containerPort | int | `8889` |  |
| extraConfigMap | list | `[]` |  |
| extraSecret | list | `[]` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `""` |  |
| global.registry | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/api-gateway"` |  |
| image.tag | string | `"staging"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"api-gateway.example.domain"` |  |
| ingress.ingressClassName | string | `""` |  |
| replicaCount | int | `1` |  |
| secret.AWS_ACCESS_KEY_ID | string | `""` |  |
| secret.AWS_SECRET_ACCESS_KEY | string | `""` |  |
| services[0].name | string | `"api-gateway-public"` |  |
| services[0].port | int | `80` |  |
| services[0].protocol | string | `"TCP"` |  |
| services[0].selector.app | string | `"api-gateway"` |  |
| services[0].targetPort | int | `8889` |  |
| services[0].type | string | `"NodePort"` |  |