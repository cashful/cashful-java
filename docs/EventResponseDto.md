

# EventResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique identifier for the event |  |
|**merchantId** | **String** | ID of the merchant this event belongs to |  |
|**webhookEndpointId** | **String** | ID of the webhook endpoint this event was sent to |  |
|**type** | **String** | Event type name |  |
|**data** | **Object** | Event data payload |  |
|**status** | [**StatusEnum**](#StatusEnum) | Current delivery status of the event |  |
|**attempts** | **BigDecimal** | Number of delivery attempts |  |
|**relatedEntityId** | **String** | ID of the related entity |  [optional] |
|**relatedEntityType** | **String** | Type of the related entity |  [optional] |
|**lastAttemptAt** | **OffsetDateTime** | Timestamp of the last delivery attempt |  [optional] |
|**nextRetryAt** | **OffsetDateTime** | Timestamp for the next retry attempt |  [optional] |
|**deliveredAt** | **OffsetDateTime** | Timestamp when the event was successfully delivered |  [optional] |
|**createdAt** | **OffsetDateTime** | Timestamp when the event was created |  |
|**updatedAt** | **OffsetDateTime** | Timestamp when the event was last updated |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| DELIVERED | &quot;delivered&quot; |
| FAILED | &quot;failed&quot; |


## Implemented Interfaces

* Serializable


