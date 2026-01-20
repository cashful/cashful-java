

# CreatePaymentLinkDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**productId** | **String** | The unique identifier of the product |  [optional] |
|**customerId** | **String** | The unique identifier of the customer |  [optional] |
|**amount** | **BigDecimal** | The amount in the smallest currency unit |  [optional] |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**mode** | [**ModeEnum**](#ModeEnum) | The payment mode (e.g., &#39;payment&#39; or &#39;subscription&#39;) |  |
|**successUrl** | **String** | The URL to redirect to on successful payment |  |
|**cancelUrl** | **String** | The URL to redirect to if customer cancels |  |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| PAYMENT | &quot;payment&quot; |
| SETUP | &quot;setup&quot; |
| SUBSCRIPTION | &quot;subscription&quot; |


## Implemented Interfaces

* Serializable


