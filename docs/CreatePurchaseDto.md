

# CreatePurchaseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**customerId** | **String** | The unique identifier of the customer |  |
|**productId** | **String** | The unique identifier of the product |  |
|**amount** | **BigDecimal** | The amount in the smallest currency unit |  |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**quantity** | **BigDecimal** | The quantity of items in the purchase |  [optional] |


## Implemented Interfaces

* Serializable


