

# HostedCheckoutConfigDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | Merchant ID |  [optional] |
|**merchantAlias** | **String** | Merchant alias |  [optional] |
|**merchantLegalName** | **String** | Merchant legal name |  [optional] |
|**merchantAvatarTextPlaceholder** | **String** | Merchant avatar text placeholder |  [optional] |
|**merchantAvatarUrl** | **String** | Merchant avatar URL |  [optional] |
|**requireContact** | **Boolean** | Require contact |  [optional] |
|**requireAddress** | **Boolean** | Require address |  [optional] |
|**taxRate** | **BigDecimal** | Tax rate |  [optional] |
|**embedMode** | **Boolean** | Embed mode |  [optional] |
|**embedOrigin** | **String** | Embed origin |  [optional] |
|**methods** | [**List&lt;MethodsEnum&gt;**](#List&lt;MethodsEnum&gt;) | Enabled payment methods |  [optional] |



## Enum: List&lt;MethodsEnum&gt;

| Name | Value |
|---- | -----|
| CARD | &quot;card&quot; |
| WALLET | &quot;wallet&quot; |
| BANK | &quot;bank&quot; |


## Implemented Interfaces

* Serializable


