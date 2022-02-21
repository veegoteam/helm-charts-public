# api-gateway

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
| configMap.AWS_ACCOUNT_ID | string | `""` |  |
| configMap.AWS_REGION | string | `""` |  |
| configMap.LOGSTASH_HOST | string | `""` |  |
| configMap.QUICKSIGHT_ANALYTICS_DASHBOARD_ID | string | `"11c2aa38-4f38-470f-8dc0-950046bce999"` |  |
| configMap.QUICKSIGHT_MARKETING_DASHBOARD_ID | string | `"d4e521f9-840a-4309-889c-689194045dc6"` |  |
| configMap.QUICKSIGHT_MY_EXPERIENCE_DASHBOARD_ID | string | `"d3228250-8ebb-48e5-b959-1c176722e5cb"` |  |
| configMap.QUICKSIGHT_MY_HOME_DASHBOARD_ID | string | `"b24234ff-508e-47f6-b142-ca10d956ac0c"` |  |
| configMap.QUICKSIGHT_MY_MALFUNCTIONS_DASHBOARD_ID | string | `"06ee0fa6-c2d9-4d15-af33-500111df4734"` |  |
| configMap.QUICKSIGHT_MY_SERVICES_DASHBOARD_ID | string | `"6ea9e8bc-0a8e-4045-9dfe-b12e08bbbc5f"` |  |
| configMap.VEEGO_KAFKA_HOSTS | string | `""` |  |
| configMap.VEEGO_REDIS_HOSTS | string | `""` |  |
| configMap.VEEGO_SERVER_TIME_ZONE | string | `"Asia/Jerusalem"` |  |
| configMap.VEEGO_SIGN_OUT_URL | string | `""` |  |
| configMap.VEEGO_SQL_URL | string | `""` |  |
| configMap.VEEGO_ZIPKIN_BASE_URL | string | `""` |  |
| containerPort | int | `8889` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/api-gateway"` |  |
| image.tag | string | `"staging"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0] | string | `"api-gateway.example.domain"` |  |
| ingress.hosts[1] | string | `"dashboard.example.domain"` |  |
| ingress.ingressClassName | string | `""` |  |
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
| services[0].name | string | `"api-gateway-public"` |  |
| services[0].port | int | `80` |  |
| services[0].protocol | string | `"TCP"` |  |
| services[0].selector.app | string | `"api-gateway"` |  |
| services[0].targetPort | int | `8889` |  |
| services[0].type | string | `"NodePort"` |  |