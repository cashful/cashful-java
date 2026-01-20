

# SendEmailDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**to** | **Object** | Recipient email address(es) |  |
|**subject** | **String** | Email subject |  |
|**template** | **String** | Template name to use (if using templates) |  [optional] |
|**context** | **Object** | Context variables for template rendering |  [optional] |
|**html** | **String** | HTML content (if not using templates) |  [optional] |
|**text** | **String** | Plain text content |  [optional] |
|**from** | **String** | Sender email address |  [optional] |
|**cc** | **Object** | CC email address(es) |  [optional] |
|**bcc** | **Object** | BCC email address(es) |  [optional] |


## Implemented Interfaces

* Serializable


