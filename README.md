# dafka-producer

![Version: 0.0.4](https://img.shields.io/badge/Version-0.0.4-informational?style=flat-square)

A Helm Chart for Dafka Producer

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| name | string | `"kafka-producer"` |  |
| port | int | `3000` |  |
| replicaCount | int | `2` |  |
| image | string | `"osskit/dafka-producer:1.0.0"` |  |
| usePrometheus | bool | `true` |  |
| livenessProbe.httpGet.path | string | `"/isAlive"` |  |
| livenessProbe.httpGet.port | int | `3000` |  |
| readinessProbe.httpGet.path | string | `"/isAlive"` |  |
| readinessProbe.httpGet.port | int | `3000` |  |
| resources.requests.cpu | string | `"400m"` |  |
| resources.requests.memory | string | `"400Mi"` |  |
| resources.limits.cpu | string | `"800m"` |  |
| resources.limits.memory | string | `"800Mi"` |  |
| metrics.enabled | bool | `true` |  |
| metrics.path | string | `"/metrics"` |  |

