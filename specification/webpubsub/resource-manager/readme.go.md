## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go) && !$(track2)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: webpubsub
  clear-output-folder: true
```

``` yaml $(go) && $(track2)
license-header: MICROSOFT_MIT_NO_VERSION
module-name: sdk/resourcemanager/webpubsub/armwebpubsub
module: github.com/Azure/azure-sdk-for-go/$(module-name)
output-folder: $(go-sdk-folder)/$(module-name)
azure-arm: true
directive:
- rename-model:
    from: 'WebPubSubResource'
    to: 'ResourceInfo'
- rename-model:
    from: 'WebPubSubResourceList'
    to: 'ResourceInfoList'
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2021-04-01-preview
  - tag: package-2021-06-01-preview
  - tag: package-2021-09-01-preview
  - tag: package-2022-08-01-preview
  - tag: package-2021-10-01
  - tag: package-2023-02-01
  - tag: package-2023-03-01-preview
```

### Tag: package-2021-04-01-preview and go

These settings apply only when `--tag=package-2021-04-01-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-04-01-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2021-04-01-preview/$(namespace)
```


### Tag: package-2021-06-01-preview and go

These settings apply only when `--tag=package-2021-06-01-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-06-01-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2021-06-01-preview/$(namespace)
```

### Tag: package-2021-09-01-preview and go

These settings apply only when `--tag=package-2021-09-01-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-09-01-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2021-09-01-preview/$(namespace)
```

### Tag: package-2022-08-01-preview and go

These settings apply only when `--tag=package-2022-08-01-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2022-08-01-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2022-08-01-preview/$(namespace)
```

### Tag: package-2021-10-01 and go

These settings apply only when `--tag=package-2021-10-01 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2021-10-01' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2021-10-01/$(namespace)
```

### Tag: package-2023-02-01 and go

These settings apply only when `--tag=package-2023-02-01 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2023-02-01' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2023-02-01/$(namespace)
```

### Tag: package-2023-03-01-preview and go

These settings apply only when `--tag=package-2023-03-01-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2023-03-01-preview' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2023-03-01-preview/$(namespace)
```