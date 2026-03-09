

# InitiatePaymentResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**iveriParams** | [**IveriParamsDto**](IveriParamsDto.md) | Parameters to POST to iVeri 3DS endpoint (only in live mode) |  [optional] |
|**iVeri3dsEndpoint** | **String** | iVeri 3DS endpoint URL to POST the parameters to (only in live mode) |  [optional] |
|**sandboxMode** | **Boolean** | Whether sandbox mode is active |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Payment status (only in sandbox mode) |  [optional] |
|**paymentIntentId** | **String** | Payment intent ID |  [optional] |
|**transactionId** | **String** | Transaction ID (only in sandbox mode on success) |  [optional] |
|**authCode** | **String** | Authorization code (only in sandbox mode on success) |  [optional] |
|**amount** | **BigDecimal** | Payment amount in smallest currency unit |  [optional] |
|**currency** | **String** | Currency code |  [optional] |
|**reason** | **String** | Reason for failure (only in sandbox mode on failure) |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| SUCCEEDED | &quot;succeeded&quot; |
| FAILED | &quot;failed&quot; |


## Implemented Interfaces

* Serializable


