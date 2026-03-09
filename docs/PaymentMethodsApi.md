# PaymentMethodsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deletePaymentMethod**](PaymentMethodsApi.md#deletePaymentMethod) | **DELETE** /api/canary/payment-methods/{id} | Delete Payment Method |
| [**listPaymentMethods**](PaymentMethodsApi.md#listPaymentMethods) | **GET** /api/canary/payment-methods | List Payment Methods |
| [**retrievePaymentMethod**](PaymentMethodsApi.md#retrievePaymentMethod) | **GET** /api/canary/payment-methods/{id} | Retrieve Payment Method |


<a id="deletePaymentMethod"></a>
# **deletePaymentMethod**
> Object deletePaymentMethod(id)

Delete Payment Method

Detaches and deletes a saved payment method from a customer.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentMethodsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentMethodsApi apiInstance = new PaymentMethodsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment method
    try {
      Object result = apiInstance.deletePaymentMethod(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentMethodsApi#deletePaymentMethod");
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
| **id** | **String**| The unique identifier of the payment method | |

### Return type

**Object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment method successfully deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listPaymentMethods"></a>
# **listPaymentMethods**
> ListPaymentMethodsResponseDto listPaymentMethods(limit, offset, filter, sort, order, merchantId, customerId)

List Payment Methods

Lists saved payment methods for a specific customer.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentMethodsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentMethodsApi apiInstance = new PaymentMethodsApi(defaultClient);
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of items to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of items to skip
    String filter = "{\"ids\":[\"prod_123\",\"prod_456\"]}"; // String | JSON string used for dynamic filtering
    String sort = "createdAt"; // String | Field name to sort by
    String order = "DESC"; // String | Sort direction
    String merchantId = "merchantId_example"; // String | The ID of the merchant. If omitted, defaults to the authenticated merchant.
    String customerId = "customerId_example"; // String | Customer ID to filter by
    try {
      ListPaymentMethodsResponseDto result = apiInstance.listPaymentMethods(limit, offset, filter, sort, order, merchantId, customerId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentMethodsApi#listPaymentMethods");
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
| **filter** | **String**| JSON string used for dynamic filtering | [optional] |
| **sort** | **String**| Field name to sort by | [optional] |
| **order** | **String**| Sort direction | [optional] |
| **merchantId** | **String**| The ID of the merchant. If omitted, defaults to the authenticated merchant. | [optional] |
| **customerId** | **String**| Customer ID to filter by | [optional] |

### Return type

[**ListPaymentMethodsResponseDto**](ListPaymentMethodsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved payment methods list |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="retrievePaymentMethod"></a>
# **retrievePaymentMethod**
> PaymentMethodResponseDto retrievePaymentMethod(id)

Retrieve Payment Method

Gets the non-sensitive details of a saved card (e.g., brand, last 4).

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentMethodsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentMethodsApi apiInstance = new PaymentMethodsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment method
    try {
      PaymentMethodResponseDto result = apiInstance.retrievePaymentMethod(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentMethodsApi#retrievePaymentMethod");
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
| **id** | **String**| The unique identifier of the payment method | |

### Return type

[**PaymentMethodResponseDto**](PaymentMethodResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved payment method details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

