

# FileDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique identifier |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |
|**deletedAt** | **OffsetDateTime** |  |  [optional] |
|**key** | **String** |  |  |
|**bucket** | **String** |  |  |
|**filename** | **String** |  |  |
|**mimeType** | **String** |  |  |
|**size** | **BigDecimal** |  |  |
|**tags** | **List&lt;String&gt;** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**checksum** | **String** |  |  [optional] |
|**isPublic** | **Boolean** |  |  |
|**relatedEntityId** | **String** |  |  [optional] |
|**relatedEntityType** | **String** |  |  [optional] |
|**uploadedById** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| UPLOADED | &quot;uploaded&quot; |
| FAILED | &quot;failed&quot; |
| DELETED | &quot;deleted&quot; |


## Implemented Interfaces

* Serializable


