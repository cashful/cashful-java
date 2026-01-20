

# DebitReturnResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | [**StatusEnum**](#StatusEnum) | Payment status after 3DS authentication |  |
|**merchantReference** | **String** | Merchant reference for the payment |  |
|**paymentIntentId** | **String** | Payment intent ID |  [optional] |
|**transactionId** | **String** | Transaction ID if payment succeeded |  [optional] |
|**authCode** | **String** | Authorization code from payment gateway |  [optional] |
|**reason** | **String** | Reason for failure if payment failed |  [optional] |
|**amount** | **BigDecimal** | Payment amount in smallest currency unit |  [optional] |
|**currency** | **String** | Currency code |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| SUCCEEDED | &quot;succeeded&quot; |
| FAILED | &quot;failed&quot; |
| PENDING | &quot;pending&quot; |


## Implemented Interfaces

* Serializable


