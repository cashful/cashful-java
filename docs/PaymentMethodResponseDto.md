

# PaymentMethodResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique payment method identifier |  |
|**customerId** | **String** | Customer ID this payment method belongs to |  |
|**type** | **String** | Payment method type (e.g., card, mobile_money) |  |
|**provider** | **String** | Payment provider name (e.g., iveri, mpesa) |  |
|**brand** | **String** | Card brand (e.g., Visa, Mastercard) |  [optional] |
|**last4** | **String** | Last 4 digits of card number |  [optional] |
|**expiryMonth** | **BigDecimal** | Card expiry month (1-12) |  [optional] |
|**expiryYear** | **BigDecimal** | Card expiry year |  [optional] |
|**phoneNumber** | **String** | Phone number for mobile money |  [optional] |
|**isDefault** | **Boolean** | Whether this is the default payment method |  |
|**createdAt** | **OffsetDateTime** | When the payment method was created |  |
|**updatedAt** | **OffsetDateTime** | When the payment method was last updated |  |


## Implemented Interfaces

* Serializable


