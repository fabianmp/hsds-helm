# hsds

![Version: 0.1.2](https://img.shields.io/badge/Version-0.1.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.6.3](https://img.shields.io/badge/AppVersion-v0.6.3-informational?style=flat-square)

A Helm chart for [HSDS](https://github.com/HDFGroup/hsds)

**Homepage:** <https://github.com/HDFGroup/hsds>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Fabian Zach | <fabian.zach@methodpark.de> | <https://github.com/fabianmp> |

## Source Code

* <https://github.com/fabianmp/hsds-helm>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| accessControl.groups | list | `[]` | List of groups for authentication (see `values.yaml` for format) |
| accessControl.users | list | `[]` | List of users for authentication (see `values.yaml` for format) |
| affinity | object | `{}` | Affinity for pods |
| config.common | object | `{"log_level":"WARNING"}` | Override common configuration values for service and data node |
| config.dataNode | object | `{}` | Override configuration values for data node |
| config.serviceNode | object | `{}` | Override configuration values for service node |
| fullnameOverride | string | `""` | Override full name of this release |
| image.pullPolicy | string | `"IfNotPresent"` | Image pull policy |
| image.repository | string | `"hdfgroup/hsds"` | HSDS image |
| image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| imagePullSecrets | list | `[]` | Image pull secrets for HSDS pod |
| ingress.annotations | object | `{}` | Annotations to add to ingress |
| ingress.enabled | bool | `false` | Enable ingress |
| ingress.hosts | list | `[{"host":"chart-example.local","paths":[]}]` | Ingress host configuration |
| ingress.tls | list | `[]` | Ingress TLS configuration |
| nameOverride | string | `""` | Override name of this release |
| nodeSelector | object | `{}` | Node selector for pods |
| podAnnotations | object | `{}` | Additional annotations to add to pod |
| podSecurityContext | object | `{}` | Configure pod security context |
| replicaCount | int | `1` | Number of HSDS nodes |
| resources.dataNode | object | `{}` | Resources for the data node container |
| resources.serviceNode | object | `{}` | Resources for the service node container |
| securityContext | object | `{}` | Configure container security context |
| service.port | int | `80` | Service port |
| service.type | string | `"ClusterIP"` | Type of service |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` | Tolerations for pods |