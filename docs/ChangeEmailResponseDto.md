

# ChangeEmailResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | **Boolean** | Indicates if request was successful |  |
|**message** | [**MessageEnum**](#MessageEnum) | Status message of email change process |  [optional] |
|**user** | [**SessionUserDto**](SessionUserDto.md) | User object |  [optional] |



## Enum: MessageEnum

| Name | Value |
|---- | -----|
| EMAIL_UPDATED | &quot;Email updated&quot; |
| VERIFICATION_EMAIL_SENT | &quot;Verification email sent&quot; |


## Implemented Interfaces

* Serializable


