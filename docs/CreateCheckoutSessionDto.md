

# CreateCheckoutSessionDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**customerId** | **String** | The unique identifier of the customer |  [optional] |
|**productId** | **String** | The unique identifier of the product |  [optional] |
|**successUrl** | **String** | The URL to redirect to on successful payment |  |
|**cancelUrl** | **String** | The URL to redirect to if customer cancels |  |
|**lineItems** | [**List&lt;LineItemDto&gt;**](LineItemDto.md) | Array of line items for the checkout |  [optional] |
|**totalAmount** | **BigDecimal** | The total amount in the smallest currency unit |  [optional] |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**mode** | **String** | The checkout mode (e.g., &#39;payment&#39;) |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  |


## Implemented Interfaces

* Serializable


