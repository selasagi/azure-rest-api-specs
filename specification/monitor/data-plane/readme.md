# MonitorClient
    
> see https://aka.ms/autorest

This is the AutoRest configuration file for MonitorClient.



---
## Getting Started 
To build the SDK for MonitorClient, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information 
These are the global settings for the MonitorClient API.

``` yaml
title: MonitorClient
description: Monitor Client
openapi-type: data-plane
tag: package-2017-05
```

### Tag: package-2017-05

These settings apply only when `--tag=package-2017-05` is specified on the command line.

``` yaml $(tag) == 'package-2017-05'
input-file:
- microsoft.insights/2014-04-01/usageMetrics_API.json
- microsoft.insights/2015-04-01/activityLogs_API.json
- microsoft.insights/2015-04-01/eventCategories_API.json
- microsoft.insights/2015-04-01/tenantActivityLogs_API.json
- microsoft.insights/2017-05-01-preview/metricDefinitions_API.json
- microsoft.insights/2017-05-01-preview/metrics_API.json
```

### Tag: package-2016-09

These settings apply only when `--tag=package-2016-09` is specified on the command line.

``` yaml $(tag) == 'package-2016-09'
input-file:
- microsoft.insights/2014-04-01/usageMetrics_API.json
- microsoft.insights/2015-04-01/activityLogs_API.json
- microsoft.insights/2015-04-01/eventCategories_API.json
- microsoft.insights/2015-04-01/tenantActivityLogs_API.json
- microsoft.insights/2016-03-01/metricDefinitions_API.json
- microsoft.insights/2016-09-01/metrics_API.json
```

---
# Code Generation


## C# 

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  payload-flattening-threshold: 1
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.Monitor
  output-folder: $(csharp-sdks-folder)/Monitor/Management.Monitor/Generated/Monitor
  clear-output-folder: true
```


## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: insights
  clear-output-folder: true
```

### Tag: package-2017-05 and go

These settings apply only when `--tag=package-2017-05 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2017-05' && $(go)
output-folder: $(go-sdk-folder)/services/monitor/2017-05-01/insights
```

### Tag: package-2016-09 and go

These settings apply only when `--tag=package-2016-09 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2016-09' && $(go)
output-folder: $(go-sdk-folder)/services/monitor/2016-09-01/insights
```


## Python

These settings apply only when `--python` is specified on the command line.

``` yaml $(python)
python:
  # override the default output folder
  output-folder: $(output-folder)/python
  license-header: MICROSOFT_MIT_NO_VERSION
  payload-flattening-threshold: 2
  namespace: azure.monitor
```

## Java

These settings apply only when `--java` is specified on the command line.

``` yaml $(java)
java:
  # override the default output folder
  output-folder: $(output-folder)/azure-mgmt-monitor/src/main/java/com/microsoft/azure/management/monitor
  license-header: MICROSOFT_MIT_NO_VERSION
  payload-flattening-threshold: 2
  namespace: com.microsoft.azure.management.monitor
```