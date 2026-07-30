# Agent guidance

Read [`CONTRIBUTING.md`](CONTRIBUTING.md) first. This file records only the
agent-specific delta.

- Do not edit `index.yaml` or add a `.tgz` file to fix or simulate a release.
  Both are produced by the platform-internal publication workflow.
- There is no chart source, build, test, or lint target in this repository.
  Do not invent a local check; validate source changes in
  `airbyte-platform-internal` and rely on the publication workflow for this
  artifact surface.
