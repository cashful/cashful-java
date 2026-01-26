

# UpdatePaymentLinkDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | The name of the payment link |  [optional] |
|**description** | **String** | A description of the payment link |  [optional] |
|**active** | **Boolean** | Whether the payment link is active |  [optional] |
|**totalAmount** | **BigDecimal** |  |  [optional] |
|**successUrl** | **String** | The URL to redirect to on successful payment |  [optional] |
|**cancelUrl** | **String** | The URL to redirect to if customer cancels |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  |
|**hostedCheckoutConfig** | [**HostedCheckoutConfigDto**](HostedCheckoutConfigDto.md) | Configuration for the hosted checkout page |  [optional] |


## Implemented Interfaces

* Serializable


