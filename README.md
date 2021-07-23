# dafka-producer

![Version: 0.1.5](https://img.shields.io/badge/Version-0.1.5-informational?style=flat-square)

A Helm Chart for Dafka Producer

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| name | string | `"kafka-producer"` | name for this producer |
| port | int | `3000` | the port to use |
| replicaCount | int | `2` | pod count |
| image.name | string | `"osskit/dafka-producer"` | the image name to use |
| image.tag | string | `"2.0"` | the image tag to use |
| healthcheckPath | string | `"/isAlive"` | the path for healthchecks, used for liveness and readiness |
| resources.requests.cpu | string | `"400m"` | cpu requests |
| resources.requests.memory | string | `"400Mi"` | memory requests |
| resources.limits.cpu | string | `"800m"` | cpu limits |
| resources.limits.memory | string | `"800Mi"` | memory limits |
| metrics.enabled | bool | `true` | should prometheus scrape this server |
| metrics.path | string | `"/metrics"` | a path prometheus should scrape metrics from |
| auth.saslUsername | string | `nil` | sasl username |
| auth.saslPassword | string | `nil` | sasl password |
| auth.saslPasswordResource | string | `nil` | gcp secret resource for sasl password |
| auth.useOpaqueSecrets | bool | `true` | mount GCP secrets to Opaque secrets |
| auth.truststore.truststoreResource | string | `nil` | gcp secret resource for truststore file |
| auth.truststore.truststorePasswordResource | string | `nil` | gcp secret resource for truststore password |

