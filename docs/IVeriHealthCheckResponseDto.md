

# IVeriHealthCheckResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | **String** | Service health status |  |
|**environment** | [**EnvironmentEnum**](#EnvironmentEnum) | Current environment mode |  |
|**timestamp** | **String** | Current server timestamp in ISO format |  |



## Enum: EnvironmentEnum

| Name | Value |
|---- | -----|
| SANDBOX | &quot;sandbox&quot; |
| LIVE | &quot;live&quot; |
| LOCAL | &quot;local&quot; |


## Implemented Interfaces

* Serializable


