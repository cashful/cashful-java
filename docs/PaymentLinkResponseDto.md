

# PaymentLinkResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**merchantId** | **String** |  |  |
|**url** | **String** |  |  |
|**productId** | **String** |  |  [optional] |
|**customerId** | **String** |  |  [optional] |
|**amount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  |
|**mode** | [**ModeEnum**](#ModeEnum) |  |  |
|**active** | **Boolean** |  |  |
|**successUrl** | **String** |  |  |
|**cancelUrl** | **String** |  |  |
|**metadata** | **Map&lt;String, Object&gt;** |  |  |
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


