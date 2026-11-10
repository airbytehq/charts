# Airbyte Helm charts

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/airbyte-v2)](https://artifacthub.io/packages/search?repo=airbyte-v2)

Official Helm charts for Airbyte self-managed deployments.

## Usage

```sh
helm repo add airbyte https://airbytehq.github.io/charts
helm repo update
helm search repo airbyte
```

## Charts

| Chart | Purpose | Deployment docs | Artifact Hub |
| --- | --- | --- | --- |
| `airbyte` | Deploy the Airbyte platform on Kubernetes. | [Deploy Airbyte](https://docs.airbyte.com/platform/deploying-airbyte/chart-v2-community) | [airbyte](https://artifacthub.io/packages/helm/airbyte-v2/airbyte) |
| `airbyte-data-plane` | Deploy a data plane for Airbyte Enterprise Flex. | [Deploy a data plane](https://docs.airbyte.com/platform/enterprise-flex/data-plane) | [airbyte-data-plane](https://artifacthub.io/packages/helm/airbyte-v2/airbyte-data-plane) |

Chart source: [airbytehq/airbyte-platform](https://github.com/airbytehq/airbyte-platform/tree/main/charts/v2).
