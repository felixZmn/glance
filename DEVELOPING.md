# Developing

## Release Workflow

Building and releasing a new version of the chart can be done with the following steps:

1. **Update the chart version**
   Ensure that the `version` and `appVersion` fields in `Chart.yaml` are updated.
2. **Update README.md**
   To ensure the README is up to date, run
   ```bash
    helm-docs
   ```
   in the root directory of the chart.
3. **Create git tag**
   Create a new git tag corresponding to the new chart version:
   ```bash
   git tag X.Y.Z
   git push origin X.Y.Z
   ```
4. **Build and publish the chart**
   ```bash
    helm package .
    helm push glance-*.tgz oci://ghcr.io/felixzmn/helm
   ```
5. **Create a GitHub Release**
