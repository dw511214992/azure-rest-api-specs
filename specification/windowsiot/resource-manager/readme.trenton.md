
## trenton

These settings apply only when `--trenton` is specified on the command line.

``` yaml $(trenton)
trenton:
    cli-name: windowsiot
    package-name: windowsiot
clear-output-folder: true
output-folder: $(trenton-output-folder)/windowsiot
overrides:
  - where:
      method: "Update"
    set:
      - BodyPosition: 2
  - where:
      method: "CreateOrUpdate"
    set:
      - BodyPosition: 2
  - where:
      property: "deviceName"
    set:
      - IdPortion: "DeviceServices"
```
