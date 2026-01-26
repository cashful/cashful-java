

# UpdateCheckoutSessionDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | **String** |  |  |
|**successUrl** | **String** | The URL to redirect to on successful payment |  [optional] |
|**failureUrl** | **String** | The URL to redirect to on failure |  [optional] |
|**cancelUrl** | **String** | The URL to redirect to on cancel |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  |
|**hostedCheckoutConfig** | [**HostedCheckoutConfigDto**](HostedCheckoutConfigDto.md) | Configuration for the hosted checkout page |  [optional] |


## Implemented Interfaces

* Serializable


