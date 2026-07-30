# Contributing

## Mental model

`airbytehq/charts` is a published Helm repository, not a source repository.
The chart source is maintained in
[airbyte-platform-internal](https://github.com/airbytehq/airbyte-platform-internal/tree/master/oss/charts/v2).

For chart changes, work in one of these source directories:

- `oss/charts/v2/airbyte`
- `oss/charts/v2/airbyte-data-plane`

Follow the source repository's contribution guidance and validation commands
there. Do not package charts or update the published index by hand in this
repository.

## Publishing

The authoritative release process is documented in
[`docs/knowledge-transfer/05-oss-release.md`](https://github.com/airbytehq/airbyte-platform-internal/blob/master/docs/knowledge-transfer/05-oss-release.md).
The platform-internal
[`publish-oss-chart.yml`](https://github.com/airbytehq/airbyte-platform-internal/blob/master/.github/workflows/publish-oss-chart.yml)
workflow packages the source charts, updates the repository index, and
publishes the artifacts here. Public releases are gated by the
`oss-public-release` environment approval.

The generated files are:

- `airbyte-*.tgz`
- `airbyte-data-plane-*.tgz`
- `index.yaml`

Do not hand-edit or hand-add those files. `artifacthub-repo.yml` contains the
Artifact Hub ownership metadata and is maintained separately.

## Consuming releases

GitHub Pages serves this repository at
https://airbytehq.github.io/charts. To consume a release:

```bash
helm repo add airbyte-v2 https://airbytehq.github.io/charts
helm repo update
helm search repo airbyte-v2 --versions
```
