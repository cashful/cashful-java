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
> ListPaymentMethodsResponseDto listPaymentMethods(limit, offset, merchantId, customerId)

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
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of records to skip
    String merchantId = "merchantId_example"; // String | The unique identifier of the merchant. If not provided, defaults to the authenticated user's active organization.
    String customerId = "customerId_example"; // String | The unique identifier of the customer
    try {
      ListPaymentMethodsResponseDto result = apiInstance.listPaymentMethods(limit, offset, merchantId, customerId);
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
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] |
| **merchantId** | **String**| The unique identifier of the merchant. If not provided, defaults to the authenticated user&#39;s active organization. | [optional] |
| **customerId** | **String**| The unique identifier of the customer | [optional] |

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

