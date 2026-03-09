

# CheckoutSessionConfirmResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**sessionId** | **String** |  |  |
|**paymentIntentId** | **String** |  |  |
|**iveriParams** | **Object** |  |  [optional] |
|**iVeri3dsEndpoint** | **String** |  |  [optional] |
|**sandboxMode** | **Boolean** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**transactionId** | **String** |  |  [optional] |
|**authCode** | **String** |  |  [optional] |
|**amount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**reason** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| SUCCEEDED | &quot;succeeded&quot; |
| FAILED | &quot;failed&quot; |


## Implemented Interfaces

* Serializable


