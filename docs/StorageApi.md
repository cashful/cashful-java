# StorageApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**storageControllerConfirmUploadCanary**](StorageApi.md#storageControllerConfirmUploadCanary) | **POST** /api/canary/storage/confirm-upload | Confirm that a file upload was completed |
| [**storageControllerDeleteCanary**](StorageApi.md#storageControllerDeleteCanary) | **DELETE** /api/canary/storage/{id} | Delete a file |
| [**storageControllerGetDownloadUrlCanary**](StorageApi.md#storageControllerGetDownloadUrlCanary) | **GET** /api/canary/storage/{id}/download-url | Get a presigned download URL for a file |
| [**storageControllerListCanary**](StorageApi.md#storageControllerListCanary) | **GET** /api/canary/storage | List files |
| [**storageControllerRequestUploadUrlCanary**](StorageApi.md#storageControllerRequestUploadUrlCanary) | **POST** /api/canary/storage/upload-url | Request a presigned URL for file upload |
| [**storageControllerRetrieveCanary**](StorageApi.md#storageControllerRetrieveCanary) | **GET** /api/canary/storage/{id} | Get file details |


<a id="storageControllerConfirmUploadCanary"></a>
# **storageControllerConfirmUploadCanary**
> FileDto storageControllerConfirmUploadCanary(confirmUploadDto)

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
      FileDto result = apiInstance.storageControllerConfirmUploadCanary(confirmUploadDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#storageControllerConfirmUploadCanary");
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

<a id="storageControllerDeleteCanary"></a>
# **storageControllerDeleteCanary**
> storageControllerDeleteCanary(id)

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
      apiInstance.storageControllerDeleteCanary(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#storageControllerDeleteCanary");
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

<a id="storageControllerGetDownloadUrlCanary"></a>
# **storageControllerGetDownloadUrlCanary**
> PresignedDownloadResponseDto storageControllerGetDownloadUrlCanary(id)

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
      PresignedDownloadResponseDto result = apiInstance.storageControllerGetDownloadUrlCanary(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#storageControllerGetDownloadUrlCanary");
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

<a id="storageControllerListCanary"></a>
# **storageControllerListCanary**
> ListFilesResponseDto storageControllerListCanary(limit, offset, tag, status, relatedEntityId, relatedEntityType)

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
      ListFilesResponseDto result = apiInstance.storageControllerListCanary(limit, offset, tag, status, relatedEntityId, relatedEntityType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#storageControllerListCanary");
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

<a id="storageControllerRequestUploadUrlCanary"></a>
# **storageControllerRequestUploadUrlCanary**
> PresignedUploadResponseDto storageControllerRequestUploadUrlCanary(requestUploadUrlDto)

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
      PresignedUploadResponseDto result = apiInstance.storageControllerRequestUploadUrlCanary(requestUploadUrlDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#storageControllerRequestUploadUrlCanary");
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

<a id="storageControllerRetrieveCanary"></a>
# **storageControllerRetrieveCanary**
> FileDto storageControllerRetrieveCanary(id)

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
      FileDto result = apiInstance.storageControllerRetrieveCanary(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling StorageApi#storageControllerRetrieveCanary");
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

