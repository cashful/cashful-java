

# PaymentLinkResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**name** | **String** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**merchantId** | **String** |  |  |
|**url** | **String** |  |  |
|**lineItems** | [**List&lt;LineItemDto&gt;**](LineItemDto.md) |  |  [optional] |
|**customerId** | **String** |  |  [optional] |
|**totalAmount** | **BigDecimal** |  |  |
|**currency** | **String** |  |  |
|**mode** | [**ModeEnum**](#ModeEnum) |  |  |
|**active** | **Boolean** |  |  |
|**successUrl** | **String** |  |  |
|**cancelUrl** | **String** |  |  |
|**metadata** | **Map&lt;String, Object&gt;** |  |  |
|**hostedCheckoutConfig** | [**HostedCheckoutConfigDto**](HostedCheckoutConfigDto.md) | Configuration for the hosted checkout page |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |
|**deletedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| PAYMENT | &quot;payment&quot; |
| SETUP | &quot;setup&quot; |
| SUBSCRIPTION | &quot;subscription&quot; |


## Implemented Interfaces

* Serializable


