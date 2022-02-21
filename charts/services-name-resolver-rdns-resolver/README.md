# services-name-resolver-rdns-resolver

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam.github.io/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configMap.LOGSTASH_HOST | string | `""` |  |
| configMap.REDIS_HOST | string | `"192.168.22.40:6379,192.168.29.184:6379,192.168.3.89:6379"` |  |
| containerPort | int | `8080` |  |
| global.imagePullSecrets | list | `[]` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| image.repository | string | `"veego/services-name-resolver-rdns-resolver"` |  |
| image.tag | string | `"staging"` |  |
| replicaCount | int | `1` |  |
| secret.REDIS_PASSWORD | string | `""` |  |