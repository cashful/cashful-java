

# PaymentIntentResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique payment intent ID |  |
|**merchantId** | **String** | Merchant ID |  |
|**customerId** | **String** | Customer ID (if associated) |  |
|**paymentMethodId** | **String** | Payment method ID (if attached) |  |
|**amount** | **BigDecimal** | Amount in smallest currency unit |  |
|**currency** | **String** | Three-letter currency code |  |
|**status** | [**StatusEnum**](#StatusEnum) | Current status of the payment intent |  |
|**mode** | [**ModeEnum**](#ModeEnum) | Mode of the payment intent |  |
|**description** | **String** | Description |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Custom metadata |  [optional] |
|**idempotencyKey** | **String** | Unique idempotency key for this payment intent |  |
|**expiresAt** | **OffsetDateTime** | When the payment intent expires |  |
|**createdAt** | **OffsetDateTime** | Creation timestamp |  |
|**updatedAt** | **OffsetDateTime** | Last update timestamp |  |
|**deletedAt** | **OffsetDateTime** | Deletion timestamp (for soft deletes) |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| INITIATION | &quot;initiation&quot; |
| REQUIRES_PAYMENT_METHOD | &quot;requires_payment_method&quot; |
| REQUIRES_CONFIRMATION | &quot;requires_confirmation&quot; |
| REQUIRES_ACTION | &quot;requires_action&quot; |
| PROCESSING | &quot;processing&quot; |
| REQUIRES_CAPTURE | &quot;requires_capture&quot; |
| SUCCEEDED | &quot;succeeded&quot; |
| FAILED | &quot;failed&quot; |
| CANCELED | &quot;canceled&quot; |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| PAYMENT | &quot;payment&quot; |
| SETUP | &quot;setup&quot; |
| SUBSCRIPTION | &quot;subscription&quot; |


## Implemented Interfaces

* Serializable


