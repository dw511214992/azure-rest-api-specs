
## trenton

These settings apply only when `--trenton` is specified on the command line.

``` yaml $(trenton)
trenton:
    cli-name: peering
    package-name: peering
clear-output-folder: true
output-folder: $(trenton-output-folder)/peering
overrides:
    - where:
        property: "peering"
      set:
        - GoTypeName: "Model"
    - where:
        property: /Peerings/CreateOrUpdate/peering/properties
      set:
        - GoTypeName: "Properties"
    - where:
        property: /Peerings/CreateOrUpdate/peering/sku
      set:
        - GoTypeName: "Sku"
    - where:
        property: /Peerings/CreateOrUpdate/peering/properties/direct
      set:
        - GoTypeName: "PropertiesDirect"
    - where:
        property: /Peerings/CreateOrUpdate/peering/properties/exchange
      set:
        - GoTypeName: "PropertiesExchange"
    - where:
        property: /Peerings/CreateOrUpdate/peering/properties/exchange/peerAsn
      set:
        - GoTypeName: "SubResource"
    - where:
        property: /Peerings/CreateOrUpdate/peering/properties/exchange/connections/bgpSession
      set:
        - GoTypeName: "BgpSession"
```
