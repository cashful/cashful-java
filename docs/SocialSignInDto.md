

# SocialSignInDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**provider** | **String** | The social provider to sign in with |  |
|**callbackURL** | **String** | Callback URL to redirect to after the user has signed in |  [optional] |
|**newUserCallbackURL** | **String** | Callback URL for new users |  [optional] |
|**errorCallbackURL** | **String** | Callback URL for errors |  [optional] |
|**disableRedirect** | **Boolean** | Disable automatic redirection to the provider |  [optional] |
|**idToken** | **Object** | ID token from provider |  [optional] |
|**scopes** | **List&lt;String&gt;** | Array of scopes to request from the provider |  [optional] |
|**requestSignUp** | **Boolean** | Explicitly request sign-up |  [optional] |
|**loginHint** | **String** | Login hint for the authorization code request |  [optional] |
|**additionalData** | **String** | Additional data for the request |  [optional] |


## Implemented Interfaces

* Serializable


