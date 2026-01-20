

# InitiatePaymentDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**amount** | **BigDecimal** | Payment amount in the smallest currency unit (e.g., cents) |  |
|**currency** | **String** | Three-letter ISO 4217 currency code |  |
|**merchantId** | **String** | The unique identifier of the merchant |  |
|**evervaultEncryptedCard** | [**EvervaultEncryptedCardDto**](EvervaultEncryptedCardDto.md) | Evervault encrypted card details |  |
|**paymentIntentId** | **String** | Payment intent ID (generated if not provided) |  [optional] |
|**maskedPan** | **String** | Masked PAN for display purposes |  [optional] |
|**tokenizeCard** | **Boolean** | Whether to tokenize the card for future use |  [optional] |
|**firstName** | **String** | Cardholder first name |  [optional] |
|**lastName** | **String** | Cardholder last name |  [optional] |
|**phoneNumber** | **String** | Cardholder phone number |  [optional] |
|**paymentDescription** | **String** | Payment description |  [optional] |
|**merchantName** | **String** | Merchant name for display |  [optional] |
|**metadata** | **Object** | Additional metadata |  [optional] |


## Implemented Interfaces

* Serializable


