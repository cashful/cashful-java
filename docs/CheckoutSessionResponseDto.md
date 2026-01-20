

# CheckoutSessionResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique identifier |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |
|**deletedAt** | **OffsetDateTime** |  |  [optional] |
|**merchantId** | **String** |  |  |
|**customerId** | **String** |  |  [optional] |
|**sessionUrl** | **String** |  |  |
|**successUrl** | **String** |  |  |
|**cancelUrl** | **String** |  |  |
|**lineItems** | [**List&lt;LineItemDto&gt;**](LineItemDto.md) |  |  [optional] |
|**totalAmount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  |
|**mode** | **String** |  |  [optional] |
|**status** | **String** |  |  |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** |  |  |


## Implemented Interfaces

* Serializable


