

# CreateProductDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**name** | **String** | The name of the product |  |
|**description** | **String** | A description of the product |  [optional] |
|**amount** | **BigDecimal** | The price of the product in the smallest currency unit |  [optional] |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**active** | **Boolean** | Whether the product is active |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  |


## Implemented Interfaces

* Serializable


