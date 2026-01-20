

# RequestPasswordResetDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**email** | **String** | The email address of user to send a password reset email to |  |
|**redirectTo** | **String** | The URL to redirect user to reset their password. If token isn&#39;t valid or expired, it&#39;ll be redirected with a query parameter &#x60;?error&#x3D;INVALID_TOKEN&#x60;. If token is valid, it&#39;ll be redirected with a query parameter &#x60;?token&#x3D;VALID_TOKEN&#x60; |  [optional] |


## Implemented Interfaces

* Serializable


