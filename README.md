# dafka-producer

![Version: 0.0.5](https://img.shields.io/badge/Version-0.0.5-informational?style=flat-square)

A Helm Chart for Dafka Producer

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| name | string | `"kafka-producer"` | name for this producer |
| port | int | `3000` | the port to use |
| replicaCount | int | `2` | pod count |
| image.name | string | `"osskit/dafka-producer"` | the image name to use |
| image.tag | string | `"1.0.0"` | the image tag to use |
| healthcheckPath | string | `"/isAlive"` | the path for healthchecks, used for liveness and readiness |
| resources.requests.cpu | string | `"400m"` | cpu requests |
| resources.requests.memory | string | `"400Mi"` | memory requests |
| resources.limits.cpu | string | `"800m"` | cpu limits |
| resources.limits.memory | string | `"800Mi"` | memory limits |
| metrics.enabled | bool | `true` | should prometheus scrape this server |
| metrics.path | string | `"/metrics"` | a path prometheus should scrape metrics from |

