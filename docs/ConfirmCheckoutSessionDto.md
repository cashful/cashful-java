

# ConfirmCheckoutSessionDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**evervaultEncryptedCard** | [**EvervaultEncryptedCardDto**](EvervaultEncryptedCardDto.md) | Evervault encrypted card details |  |
|**maskedPan** | **String** | Masked PAN for display purposes |  [optional] |
|**tokenizeCard** | **Boolean** | Whether to tokenize the card for future use |  [optional] |
|**firstName** | **String** | Cardholder first name |  [optional] |
|**lastName** | **String** | Cardholder last name |  [optional] |
|**phoneNumber** | **String** | Cardholder phone number |  [optional] |
|**paymentDescription** | **String** | Payment description |  [optional] |
|**merchantName** | **String** | Merchant name for display |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Additional metadata |  [optional] |


## Implemented Interfaces

* Serializable


