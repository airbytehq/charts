# Airbyte Helm charts

This repository is the published artifact surface for Airbyte's v2 Helm charts.
GitHub Pages serves it as a Helm repository at
https://airbytehq.github.io/charts.

Add the repository and search or install published charts with Helm:

```bash
helm repo add airbyte-v2 https://airbytehq.github.io/charts
helm repo update
helm search repo airbyte-v2 --versions
```

This is not the chart source repository. Chart source lives in
[airbyte-platform-internal](https://github.com/airbytehq/airbyte-platform-internal/tree/master/oss/charts/v2):

- `oss/charts/v2/airbyte`
- `oss/charts/v2/airbyte-data-plane`

Chart releases are published by
[the OSS chart workflow](https://github.com/airbytehq/airbyte-platform-internal/blob/master/.github/workflows/publish-oss-chart.yml).
The `.tgz` packages and `index.yaml` are release automation output: do not
hand-edit or add them here. The hand-editable repository files are
`artifacthub-repo.yml` and these root documentation files.
