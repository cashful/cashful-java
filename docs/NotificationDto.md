

# NotificationDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channel** | [**ChannelEnum**](#ChannelEnum) | Notification channel |  |
|**email** | [**SendEmailDto**](SendEmailDto.md) | Email notification data |  [optional] |
|**sms** | [**SendSmsDto**](SendSmsDto.md) | SMS notification data |  [optional] |



## Enum: ChannelEnum

| Name | Value |
|---- | -----|
| EMAIL | &quot;email&quot; |
| SMS | &quot;sms&quot; |


## Implemented Interfaces

* Serializable


