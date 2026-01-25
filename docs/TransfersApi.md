# TransfersApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTransfer**](TransfersApi.md#createTransfer) | **POST** /api/canary/transfers | Create P2P Transfer |
| [**listTransfers**](TransfersApi.md#listTransfers) | **GET** /api/canary/transfers | List Transfers |


<a id="createTransfer"></a>
# **createTransfer**
> TransferResponseDto createTransfer(createTransferDto)

Create P2P Transfer

(Wallet-Enabling) Moves funds from one CustomerBalance to another CustomerBalance. This is the P2P feature.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.TransfersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    TransfersApi apiInstance = new TransfersApi(defaultClient);
    CreateTransferDto createTransferDto = new CreateTransferDto(); // CreateTransferDto | Transfer details
    try {
      TransferResponseDto result = apiInstance.createTransfer(createTransferDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransfersApi#createTransfer");
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
| **createTransferDto** | [**CreateTransferDto**](CreateTransferDto.md)| Transfer details | |

### Return type

[**TransferResponseDto**](TransferResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Transfer created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **402** | Insufficient sender balance |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listTransfers"></a>
# **listTransfers**
> ListTransfersResponseDto listTransfers(limit, offset, merchantId)

List Transfers

Lists transfers for a specific merchant with pagination.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.TransfersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    TransfersApi apiInstance = new TransfersApi(defaultClient);
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of items to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of items to skip
    String merchantId = "merchantId_example"; // String | Filter by merchant ID. If omitted, defaults to the authenticated merchant.
    try {
      ListTransfersResponseDto result = apiInstance.listTransfers(limit, offset, merchantId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransfersApi#listTransfers");
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
| **limit** | **BigDecimal**| Maximum number of items to return | [optional] |
| **offset** | **BigDecimal**| Number of items to skip | [optional] |
| **merchantId** | **String**| Filter by merchant ID. If omitted, defaults to the authenticated merchant. | [optional] |

### Return type

[**ListTransfersResponseDto**](ListTransfersResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved transfers |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

