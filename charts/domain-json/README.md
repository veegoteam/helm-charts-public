# domain-json

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
| configMap.BIND | string | `"[::]:80"` |  |
| configMap.LOGSTASH_HOST | string | `""` |  |
| containerPort | int | `8889` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/domain-json"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| services[0].annotations."service.beta.kubernetes.io/aws-load-balancer-backend-protocol" | string | `"http"` |  |
| services[0].name | string | `"domain-json-public"` |  |
| services[0].port | int | `80` |  |
| services[0].protocol | string | `"TCP"` |  |
| services[0].selector.app | string | `"domain-json"` |  |
| services[0].targetPort | int | `8889` |  |
| services[0].type | string | `"ClusterIP"` |  |