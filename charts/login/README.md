# login

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
| configMap.APP_COOKIE_DOMAIN | string | `""` |  |
| configMap.AUTH_URL | string | `""` |  |
| configMap.LOGSTASH_HOST | string | `""` |  |
| containerPort | int | `8080` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/login"` |  |
| image.tag | string | `"staging"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0] | string | `"login.example.domain"` |  |
| ingress.ingressClassName | string | `""` |  |
| replicaCount | int | `1` |  |
| services[0].name | string | `"login"` |  |
| services[0].port | int | `80` |  |
| services[0].protocol | string | `"TCP"` |  |
| services[0].selector.app | string | `"login"` |  |
| services[0].targetPort | int | `8080` |  |
| services[0].type | string | `"NodePort"` |  |