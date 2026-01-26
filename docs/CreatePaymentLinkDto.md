

# CreatePaymentLinkDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | The name of the payment link |  [optional] |
|**description** | **String** | A description of the payment link |  [optional] |
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**lineItems** | [**List&lt;LineItemDto&gt;**](LineItemDto.md) | Array of line items for the checkout |  [optional] |
|**customerId** | **String** | The unique identifier of the customer |  [optional] |
|**totalAmount** | **BigDecimal** | The total amount in the smallest currency unit |  |
|**currency** | **String** | The three-letter ISO 4217 currency code |  |
|**mode** | [**ModeEnum**](#ModeEnum) | The payment mode (e.g., &#39;payment&#39; or &#39;subscription&#39;) |  |
|**successUrl** | **String** | The URL to redirect to on successful payment |  |
|**cancelUrl** | **String** | The URL to redirect to if customer cancels |  |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  |
|**hostedCheckoutConfig** | [**HostedCheckoutConfigDto**](HostedCheckoutConfigDto.md) | Configuration for the hosted checkout page |  [optional] |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| PAYMENT | &quot;payment&quot; |
| SETUP | &quot;setup&quot; |
| SUBSCRIPTION | &quot;subscription&quot; |


## Implemented Interfaces

* Serializable


