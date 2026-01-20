# CheckoutsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCheckoutSession**](CheckoutsApi.md#createCheckoutSession) | **POST** /api/canary/checkout/sessions | Create Hosted Checkout |
| [**listCheckoutSessions**](CheckoutsApi.md#listCheckoutSessions) | **GET** /api/canary/checkout/sessions | List Checkout Sessions |
| [**retrieveCheckoutSession**](CheckoutsApi.md#retrieveCheckoutSession) | **GET** /api/canary/checkout/sessions/{id} | Retrieve Checkout Session |


<a id="createCheckoutSession"></a>
# **createCheckoutSession**
> CheckoutSessionResponseDto createCheckoutSession(createCheckoutSessionDto)

Create Hosted Checkout

Creates a hosted payment page. Used for: (1) A standard e-commerce purchase, or (2) a \&quot;Pay-In\&quot; to fund a CustomerBalance.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CheckoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CheckoutsApi apiInstance = new CheckoutsApi(defaultClient);
    CreateCheckoutSessionDto createCheckoutSessionDto = new CreateCheckoutSessionDto(); // CreateCheckoutSessionDto | Checkout session details
    try {
      CheckoutSessionResponseDto result = apiInstance.createCheckoutSession(createCheckoutSessionDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutsApi#createCheckoutSession");
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
| **createCheckoutSessionDto** | [**CreateCheckoutSessionDto**](CreateCheckoutSessionDto.md)| Checkout session details | |

### Return type

[**CheckoutSessionResponseDto**](CheckoutSessionResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Checkout session created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="listCheckoutSessions"></a>
# **listCheckoutSessions**
> ListCheckoutSessionsResponseDto listCheckoutSessions(merchantId, limit, offset, status)

List Checkout Sessions

Lists checkout sessions

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CheckoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CheckoutsApi apiInstance = new CheckoutsApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant. This parameter is required.
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of records to skip
    String status = "status_example"; // String | The status to filter checkout sessions
    try {
      ListCheckoutSessionsResponseDto result = apiInstance.listCheckoutSessions(merchantId, limit, offset, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutsApi#listCheckoutSessions");
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
| **merchantId** | **String**| The ID of the merchant. This parameter is required. | |
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] |
| **status** | **String**| The status to filter checkout sessions | [optional] |

### Return type

[**ListCheckoutSessionsResponseDto**](ListCheckoutSessionsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved checkout sessions |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="retrieveCheckoutSession"></a>
# **retrieveCheckoutSession**
> CheckoutSessionResponseDto retrieveCheckoutSession(id)

Retrieve Checkout Session

Retrieves details of a specific checkout session

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CheckoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CheckoutsApi apiInstance = new CheckoutsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the checkout session
    try {
      CheckoutSessionResponseDto result = apiInstance.retrieveCheckoutSession(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutsApi#retrieveCheckoutSession");
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
| **id** | **String**| The unique identifier of the checkout session | |

### Return type

[**CheckoutSessionResponseDto**](CheckoutSessionResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved checkout session |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

