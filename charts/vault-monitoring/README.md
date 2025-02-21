# vault-monitoring

![Version: 0.4.2](https://img.shields.io/badge/Version-0.4.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

monitor your vault server from within Kubernetes' prometheus

**Homepage:** <https://github.com/adfinis/helm-charts/tree/main/charts/vault-monitoring>

## Maintainers
This chart is maintained by [Adfinis](https://adfinis.com/?pk_campaign=github&pk_kwd=helm-charts).

## Source Code

* <https://github.com/adfinis/helm-charts/tree/main/charts/vault-monitoring>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| fullnameOverride | string | `""` | specifies the full name override to be used for helm |
| nameOverride | string | `""` | specifies the name override to be used for helm |
| prometheusRules.enabled | bool | `false` | wether or not the prometheus alerts are enabled |
| prometheusRules.labels | object | `{}` | labels to set in the prometheus alerts |
| prometheusRules.namespace | string | `""` | set namespace where the prometheusRules will be created |
| prometheusRules.rules | list | list of predefined alerts | set of prometheus alerts to define |
| vault.auth.mount_path | string | `"auth/kubernetes"` | where the kubernetes auth is mounted on vault |
| vault.auth.role | string | `"metrics"` | the vault role to use for connection |
| vault.ca | string | `""` | if set a secret is created that must be mounted in Prometheus for the ServiceMonitoring to work |
| vault.ca_path | string | `"/etc/vault/ssl/ca.crt"` | the CA path to include in the configuration |
| vault.ip | string | `"10.1.2.3"` | the vault ip to connect to |
| vault.port | int | `443` | the vault port  to connect to |
| vault.portName | string | `"https"` | the vault portName to use in the services |
| vault.scheme | string | `"https"` | the scheme to use for connection |
| vault.serverName | string | `"vault.example.com"` | the vault servername |
| vault.service.selector | object | `{}` | definition of the  vault service selector for endpoint selection. Keep empty for using ExternalName |
| vault.service.type | string | `"ExternalName"` | which type the vault service has. For connecting to an external vault server, choose ExternalName |
| vault.serviceMonitor.authentication | bool | `true` | Specify to enable authentication |
| vault.serviceMonitor.bearerTokenFile | string | `"/etc/prometheus/config_out/.vault-token"` | Specify a bearerTokenFile for authentication. Keep empty for Unauthenticated access |
| vault.serviceMonitor.create | bool | `true` | wheter or not the serviceMonitor should be created |
| vault.serviceMonitor.labels | object | `{}` | labels to set on the vault serviceMonitor |
| vault.serviceMonitor.scrapeTimeout | string | `"30s"` | scrapeTimeout of the serviceMonitor |

## About this chart

Adfinis fights for a software world that is more open, where the quality is
better and where software must be accessible to everyone. This chart
is part of the action behind this commitment. Feel free to
[contact](https://adfinis.com/kontakt/?pk_campaign=github&pk_kwd=helm-charts)
us if you have any questions.

## License

This Helm chart is free software: you can redistribute it and/or modify it under the terms
of the GNU Affero General Public License as published by the Free Software Foundation,
version 3 of the License.

----------------------------------------------
Autogenerated from chart metadata using [helm-docs](https://github.com/norwoodj/helm-docs/)
