# WordPress Helm Chart

This Helm chart deploys a WordPress application with a MySQL database on Kubernetes.

## Prerequisites

- Kubernetes 1.16+
- Helm 3.0+

## Installing the Chart

To install the chart with the release name `my-wordpress`:

```bash
helm install my-wordpress .
```

## Uninstalling the Chart

To uninstall/delete the `my-wordpress` deployment:

```bash
helm delete my-wordpress
```

## Configuration

The following table lists the configurable parameters of the WordPress chart and their default values.

| Parameter | Description | Default |
| --------- | ----------- | ------- |
| `image.repository` | WordPress image repository | `wordpress` |
| `image.tag` | WordPress image tag | `6.5.2-apache` |
| `image.pullPolicy` | Image pull policy | `IfNotPresent` |
| `service.type` | Kubernetes service type | `ClusterIP` |
| `service.port` | WordPress service port | `80` |
| `wordpress.replicaCount` | Number of WordPress replicas | `1` |
| `wordpress.wordpressBlogName` | WordPress blog name | `"My WordPress Site"` |
| `wordpress.wordpressEmail` | WordPress admin email | `"admin@example.com"` |
| `wordpress.database.host` | Database host | `wordpress-mysql` |
| `wordpress.database.name` | Database name | `wordpress` |
| `wordpress.database.user` | Database user | `wordpress` |
| `mysql.enabled` | Deploy MySQL database | `true` |
| `mysql.rootPassword` | MySQL root password | `"rootpassword"` |
| `mysql.password` | MySQL user password | `"wordpresspassword"` |
| `ingress.enabled` | Enable ingress controller | `false` |

For more information, see the `values.yaml` file.
