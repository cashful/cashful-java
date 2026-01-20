

# CreateTransferDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**fromCustomerId** | **String** | The unique identifier of the customer sending the transfer |  |
|**toCustomerId** | **String** | The unique identifier of the customer receiving the transfer |  |
|**amount** | **BigDecimal** | The amount to transfer in the smallest currency unit |  |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**description** | **String** | Optional description for the transfer |  [optional] |


## Implemented Interfaces

* Serializable


