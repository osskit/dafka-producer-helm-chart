# dafka-producer

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square)

A Helm Chart for Dafka Producer

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| name | string | `"kafka-producer"` | name for this producer |
| port | int | `3000` | the port to use |
| replicaCount | int | `1` | pod count |
| image.name | string | `"osskit/dafka-producer"` | the image name to use |
| image.tag | string | `"2.1"` | the image tag to use |
| healthcheckPath | string | `"/isAlive"` | the path for healthchecks, used for liveness and readiness |
| resources.requests.cpu | string | `"50m"` | cpu requests |
| resources.requests.memory | string | `"100Mi"` | memory requests |
| resources.limits.cpu | string | `"200m"` | cpu limits |
| resources.limits.memory | string | `"400Mi"` | memory limits |
| metrics.enabled | bool | `true` | should prometheus scrape this server |
| metrics.path | string | `"/metrics"` | a path prometheus should scrape metrics from |
| correlationId.enabled | bool | `true` | should enforce correlation header being present in the record |
| correlationId.header | string | `"x-correlation-id"` | the header of the correlation id |
| auth.enabled | bool | `false` | should use authentication |
| auth.saslUsername | string | `nil` | sasl username |
| auth.saslPassword | string | `nil` | sasl password (not encrypted) |
| auth.secrets.useOpaqueSecrets | bool | `true` | should mount secrets to opaque secrets |
| auth.secrets.useTrustsore | bool | `false` | should use truststore |
| auth.secrets.gcp.saslPasswordResource | string | `nil` | gcp secret resource for sasl password |
| auth.secrets.gcp.truststoreResource | string | `nil` | gcp secret resource for truststore file |
| auth.secrets.gcp.truststorePasswordResource | string | `nil` | gcp secret resource for truststore password |
| auth.secrets.vault.saslPasswordSecretPath | string | `nil` | vault secret path for sasl password |
| auth.secrets.vault.saslPasswordSecretKey | string | `nil` | vault secret key for sasl password |
| auth.secrets.vault.truststoreSecretPath | string | `nil` | vault secret path for truststore file |
| auth.secrets.vault.truststoreSecretKey | string | `nil` | vault secret key for truststore file |
| auth.secrets.vault.truststorePasswordSecretPath | string | `nil` | vault secret path for truststore password |
| auth.secrets.vault.truststorePasswordSecretKey | string | `nil` | vault secret key for truststore password |

