# Use Azure CLI to create and destroy vm based on ARM template

## Create vm

``` bash
az group create -n deleteme-rg -l westeurope
az group deployment create --resource-group deleteme-rg --template-file './template.json' --parameters './parameters.json'
```

## Cleanup

``` bash
az group delete -n deleteme-rg
```
