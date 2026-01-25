# AnalyticsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getAnalytics**](AnalyticsApi.md#getAnalytics) | **GET** /api/canary/analytics | Get Analytics |
| [**getAnalyticsSummary**](AnalyticsApi.md#getAnalyticsSummary) | **GET** /api/canary/analytics/summary | Get Analytics Summary |


<a id="getAnalytics"></a>
# **getAnalytics**
> AnalyticsResponseDto getAnalytics(merchantId)

Get Analytics

Retrieves transaction volume and customer growth metrics for the merchant.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    String merchantId = "merchant_123"; // String | The unique identifier of the merchant. If not provided, defaults to the authenticated user's active organization.
    try {
      AnalyticsResponseDto result = apiInstance.getAnalytics(merchantId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getAnalytics");
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
| **merchantId** | **String**| The unique identifier of the merchant. If not provided, defaults to the authenticated user&#39;s active organization. | [optional] |

### Return type

[**AnalyticsResponseDto**](AnalyticsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved analytics |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="getAnalyticsSummary"></a>
# **getAnalyticsSummary**
> AnalyticsSummaryDto getAnalyticsSummary(merchantId)

Get Analytics Summary

Retrieves a quick summary of key metrics for the merchant.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    String merchantId = "merchant_123"; // String | The unique identifier of the merchant. If not provided, defaults to the authenticated user's active organization.
    try {
      AnalyticsSummaryDto result = apiInstance.getAnalyticsSummary(merchantId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getAnalyticsSummary");
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
| **merchantId** | **String**| The unique identifier of the merchant. If not provided, defaults to the authenticated user&#39;s active organization. | [optional] |

### Return type

[**AnalyticsSummaryDto**](AnalyticsSummaryDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved analytics summary |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

