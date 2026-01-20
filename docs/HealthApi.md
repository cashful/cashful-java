# HealthApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**checkHealth**](HealthApi.md#checkHealth) | **GET** /api/canary/health | Health check endpoint |


<a id="checkHealth"></a>
# **checkHealth**
> Object checkHealth()

Health check endpoint

Performs a health check on the application and external dependencies

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.models.*;
import com.cashful.api.HealthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");

    HealthApi apiInstance = new HealthApi(defaultClient);
    try {
      Object result = apiInstance.checkHealth();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HealthApi#checkHealth");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Application and all dependencies are healthy |  -  |
| **503** | One or more health checks failed |  -  |

