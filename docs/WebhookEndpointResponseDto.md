

# WebhookEndpointResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique identifier for the webhook endpoint |  |
|**merchantId** | **String** | The merchant ID this webhook belongs to |  |
|**url** | **String** | The URL where webhook events are sent |  |
|**events** | **List&lt;String&gt;** | Array of event types subscribed to |  |
|**active** | **Boolean** | Whether the webhook endpoint is active |  |
|**metadata** | **Map&lt;String, Object&gt;** | Custom metadata attached to the webhook endpoint |  [optional] |
|**createdAt** | **OffsetDateTime** | When the webhook endpoint was created |  |
|**updatedAt** | **OffsetDateTime** | When the webhook endpoint was last updated |  |
|**deletedAt** | **OffsetDateTime** | When the webhook endpoint was deleted (soft delete) |  [optional] |


## Implemented Interfaces

* Serializable


