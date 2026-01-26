# StorageApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**confirmUpload**](StorageApi.md#confirmUpload) | **POST** /api/canary/storage/confirm-upload | Confirm that a file upload was completed |
| [**deleteFile**](StorageApi.md#deleteFile) | **DELETE** /api/canary/storage/{id} | Delete a file |
| [**getDownloadUrl**](StorageApi.md#getDownloadUrl) | **GET** /api/canary/storage/{id}/download-url | Get a presigned download URL for a file |
| [**getFileDetails**](StorageApi.md#getFileDetails) | **GET** /api/canary/storage/{id} | Get file details |
| [**listFiles**](StorageApi.md#listFiles) | **GET** /api/canary/storage | List files |
| [**requestUploadUrl**](StorageApi.md#requestUploadUrl) | **POST** /api/canary/storage/upload-url | Request a presigned URL for file upload |


<a id="confirmUpload"></a>
# **confirmUpload**
> FileDto confirmUpload(confirmUploadDto)

Confirm that a file upload was completed

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    StorageApi apiInstance = new StorageApi(defaultClient);
    ConfirmUploadDto confirmUploadDto = new ConfirmUploadDto(); // ConfirmUploadDto | 
    try {
      FileDto result = apiInstance.confirmUpload(confirmUploadDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#confirmUpload");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **confirmUploadDto** | [**ConfirmUploadDto**](ConfirmUploadDto.md)|  | |

### Return type

[**FileDto**](FileDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="deleteFile"></a>
# **deleteFile**
> deleteFile(id)

Delete a file

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String id = "id_example"; // String | File ID
    try {
      apiInstance.deleteFile(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#deleteFile");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| File ID | |

### Return type

null (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="getDownloadUrl"></a>
# **getDownloadUrl**
> PresignedDownloadResponseDto getDownloadUrl(id)

Get a presigned download URL for a file

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String id = "id_example"; // String | File ID
    try {
      PresignedDownloadResponseDto result = apiInstance.getDownloadUrl(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#getDownloadUrl");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| File ID | |

### Return type

[**PresignedDownloadResponseDto**](PresignedDownloadResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="getFileDetails"></a>
# **getFileDetails**
> FileDto getFileDetails(id)

Get file details

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    StorageApi apiInstance = new StorageApi(defaultClient);
    String id = "id_example"; // String | File ID
    try {
      FileDto result = apiInstance.getFileDetails(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#getFileDetails");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| File ID | |

### Return type

[**FileDto**](FileDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listFiles"></a>
# **listFiles**
> ListFilesResponseDto listFiles(limit, offset, tag, status, relatedEntityId, relatedEntityType)

List files

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    StorageApi apiInstance = new StorageApi(defaultClient);
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of records to skip
    String tag = "tag_example"; // String | Filter by tag
    String status = "pending"; // String | 
    String relatedEntityId = "relatedEntityId_example"; // String | 
    String relatedEntityType = "relatedEntityType_example"; // String | 
    try {
      ListFilesResponseDto result = apiInstance.listFiles(limit, offset, tag, status, relatedEntityId, relatedEntityType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#listFiles");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] |
| **tag** | **String**| Filter by tag | [optional] |
| **status** | **String**|  | [optional] [enum: pending, uploaded, failed, deleted] |
| **relatedEntityId** | **String**|  | [optional] |
| **relatedEntityType** | **String**|  | [optional] |

### Return type

[**ListFilesResponseDto**](ListFilesResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="requestUploadUrl"></a>
# **requestUploadUrl**
> PresignedUploadResponseDto requestUploadUrl(requestUploadUrlDto)

Request a presigned URL for file upload

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.StorageApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    StorageApi apiInstance = new StorageApi(defaultClient);
    RequestUploadUrlDto requestUploadUrlDto = new RequestUploadUrlDto(); // RequestUploadUrlDto | 
    try {
      PresignedUploadResponseDto result = apiInstance.requestUploadUrl(requestUploadUrlDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#requestUploadUrl");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **requestUploadUrlDto** | [**RequestUploadUrlDto**](RequestUploadUrlDto.md)|  | |

### Return type

[**PresignedUploadResponseDto**](PresignedUploadResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

