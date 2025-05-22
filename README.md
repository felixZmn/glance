# glance

This repository contains the Helm chart for deploying [Glance](https://github.com/glanceapp/glance) in a Kubernetes cluster.

## Values

| Key                   | Type   | Default          | Description             |
| --------------------- | ------ | ---------------- | ----------------------- |
| `replicaCount`        | int    | `1`              | The number of replicas  |
| `image.pullPolicy`    | string | `"IfNotPresent"` | The image pull policy   |
| `image.tag`           | string | `"latest"`       | The image tag           |
| `nameOverride`        | string | `""`             | The name override       |
| `fullnameOverride`    | string | `""`             | The fullname override   |
| `service.type`        | string | `"ClusterIP"`    | The service type        |
| `service.port`        | int    | `80`             | The service port        |
| `ingress.enabled`     | bool   | `false`          | The ingress enabled     |
| `ingress.className`   | string | `nginx`          | The ingress class name  |
| `ingress.annotations` | object | `{}`             | The ingress annotations |
| `ingress.hosts`       | list   | `[]`             | The ingress hosts       |
| `ingress.tls`         | list   | `[]`             | The ingress tls         |
| `config`              | object | `{}`             | The glance config yaml  |
