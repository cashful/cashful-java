

# CreatePaymentIntentDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**customerId** | **String** | The unique identifier of the customer. Optional for payment intents that don&#39;t require a customer. |  [optional] |
|**paymentMethodId** | **String** | The unique identifier of the payment method. Optional if payment method will be collected later. |  [optional] |
|**amount** | **BigDecimal** | The amount to charge in the smallest currency unit (cents) |  |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**mode** | [**ModeEnum**](#ModeEnum) | The mode of the payment intent |  [optional] |
|**description** | **String** | Optional description for the payment |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  [optional] |
|**idempotencyKey** | **String** | A unique key to prevent duplicate charges. If not provided, one will be generated. |  [optional] |
|**expiresAt** | **OffsetDateTime** | When the payment intent expires. Defaults to 24 hours from creation. |  [optional] |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| PAYMENT | &quot;payment&quot; |
| SETUP | &quot;setup&quot; |
| SUBSCRIPTION | &quot;subscription&quot; |


## Implemented Interfaces

* Serializable


