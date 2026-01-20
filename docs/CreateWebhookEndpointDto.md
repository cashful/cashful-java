

# CreateWebhookEndpointDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantId** | **String** | The ID of the merchant whose balance is being requested. If omitted, defaults to the authenticated merchant. |  [optional] |
|**url** | **String** | The URL where webhook events will be sent |  |
|**events** | **List&lt;String&gt;** | Array of event types to listen for |  |
|**metadata** | **Map&lt;String, Object&gt;** | Optional custom metadata |  [optional] |


## Implemented Interfaces

* Serializable


