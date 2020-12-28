## Azure CLI

These settings apply only when `--az` is specified on the command line.

``` yaml $(az)
az:
  extensions: operationalinsights
  package-name: azure-mgmt-operationalinsights
  namespace: azure.mgmt.operationalinsights
  disable-checks: true
  randomize-names: true
  test-unique-resource: true
az-output-folder: $(azure-cli-extension-folder)/src/operationalinsights
python-sdk-output-folder: "$(az-output-folder)/azext_operationalinsights/vendored_sdks/operationalinsights"
cli:
  cli-directive:
    - where:
        group: '*'
      hidden: true
    - where:
        group: DataExports|Workspaces
      hidden: false
```
