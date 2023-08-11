# glueops-external-secrets

![Version: 0.4.2-alpha1](https://img.shields.io/badge/Version-0.4.2--alpha1-informational?style=flat-square) ![AppVersion: v0.1.0](https://img.shields.io/badge/AppVersion-v0.1.0-informational?style=flat-square)

GlueOps Helm Chart for external-secrets with defaults to skip installing CRDs as they are installed separately and changing intervals for a faster deployment

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.external-secrets.io | external-secrets | v0.9.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| external-secrets.certController.requeueInterval | string | `"30s"` |  |
| external-secrets.crds.createClusterExternalSecret | bool | `false` | If true, create CRDs for Cluster External Secret. |
| external-secrets.crds.createClusterSecretStore | bool | `false` | If true, create CRDs for Cluster Secret Store. |
| external-secrets.crds.createPushSecret | bool | `false` | If true, create CRDs for Push Secret. |
| external-secrets.extraEnv[0].name | string | `"VAULT_SKIP_VERIFY"` |  |
| external-secrets.extraEnv[0].value | string | `"true"` |  |
| external-secrets.installCRDs | bool | `false` |  |
| external-secrets.webhook.affinity.podAntiAffinity.requiredDuringSchedulingIgnoredDuringExecution[0].labelSelector.matchExpressions[0].key | string | `"app.kubernetes.io/name"` |  |
| external-secrets.webhook.affinity.podAntiAffinity.requiredDuringSchedulingIgnoredDuringExecution[0].labelSelector.matchExpressions[0].operator | string | `"In"` |  |
| external-secrets.webhook.affinity.podAntiAffinity.requiredDuringSchedulingIgnoredDuringExecution[0].labelSelector.matchExpressions[0].values[0] | string | `"prometheus"` |  |
| external-secrets.webhook.affinity.podAntiAffinity.requiredDuringSchedulingIgnoredDuringExecution[0].namespaceSelector | object | `{}` |  |
| external-secrets.webhook.affinity.podAntiAffinity.requiredDuringSchedulingIgnoredDuringExecution[0].topologyKey | string | `"kubernetes.io/hostname"` |  |
| external-secrets.webhook.certCheckInterval | string | `"30s"` |  |
| external-secrets.webhook.hostNetwork | bool | `true` |  |
| external-secrets.webhook.port | int | `10751` |  |
