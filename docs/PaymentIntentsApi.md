# PaymentIntentsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelPaymentIntent**](PaymentIntentsApi.md#cancelPaymentIntent) | **POST** /api/canary/payment-intents/{id}/cancel | Cancel Payment Intent |
| [**confirmPaymentIntent**](PaymentIntentsApi.md#confirmPaymentIntent) | **POST** /api/canary/payment-intents/{id}/confirm | Confirm Payment Intent |
| [**createPaymentIntent**](PaymentIntentsApi.md#createPaymentIntent) | **POST** /api/canary/payment-intents | Create Payment Intent |
| [**listPaymentIntents**](PaymentIntentsApi.md#listPaymentIntents) | **GET** /api/canary/payment-intents | List Payment Intents |
| [**retrievePaymentIntent**](PaymentIntentsApi.md#retrievePaymentIntent) | **GET** /api/canary/payment-intents/{id} | Retrieve Payment Intent |


<a id="cancelPaymentIntent"></a>
# **cancelPaymentIntent**
> PaymentIntentResponseDto cancelPaymentIntent(id)

Cancel Payment Intent

Cancels a payment intent that has not yet succeeded or failed.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentIntentsApi apiInstance = new PaymentIntentsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment intent
    try {
      PaymentIntentResponseDto result = apiInstance.cancelPaymentIntent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentsApi#cancelPaymentIntent");
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
| **id** | **String**| The unique identifier of the payment intent | |

### Return type

[**PaymentIntentResponseDto**](PaymentIntentResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment intent canceled |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="confirmPaymentIntent"></a>
# **confirmPaymentIntent**
> PaymentIntentResponseDto confirmPaymentIntent(id)

Confirm Payment Intent

Confirms a payment intent that requires confirmation. This initiates the actual payment processing.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentIntentsApi apiInstance = new PaymentIntentsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment intent
    try {
      PaymentIntentResponseDto result = apiInstance.confirmPaymentIntent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentsApi#confirmPaymentIntent");
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
| **id** | **String**| The unique identifier of the payment intent | |

### Return type

[**PaymentIntentResponseDto**](PaymentIntentResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment intent confirmed and processing |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="createPaymentIntent"></a>
# **createPaymentIntent**
> PaymentIntentResponseDto createPaymentIntent(createPaymentIntentDto)

Create Payment Intent

Creates a payment intent for off-session charges. Used for subscriptions, recurring billing, or server-to-server payments with saved cards.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentIntentsApi apiInstance = new PaymentIntentsApi(defaultClient);
    CreatePaymentIntentDto createPaymentIntentDto = new CreatePaymentIntentDto(); // CreatePaymentIntentDto | Payment intent details
    try {
      PaymentIntentResponseDto result = apiInstance.createPaymentIntent(createPaymentIntentDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentsApi#createPaymentIntent");
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
| **createPaymentIntentDto** | [**CreatePaymentIntentDto**](CreatePaymentIntentDto.md)| Payment intent details | |

### Return type

[**PaymentIntentResponseDto**](PaymentIntentResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Payment intent created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **402** | Payment declined |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listPaymentIntents"></a>
# **listPaymentIntents**
> listPaymentIntents(merchantId, limit, offset, status)

List Payment Intents

Lists payment intents for a specific merchant with pagination and filtering.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentIntentsApi apiInstance = new PaymentIntentsApi(defaultClient);
    String merchantId = "merchantId_example"; // String | Filter by merchant ID
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of records to skip
    String status = "initiation"; // String | Filter by status
    try {
      apiInstance.listPaymentIntents(merchantId, limit, offset, status);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentsApi#listPaymentIntents");
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
| **merchantId** | **String**| Filter by merchant ID | |
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] [default to 50] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] [default to 0] |
| **status** | **String**| Filter by status | [optional] [enum: initiation, requires_payment_method, requires_confirmation, requires_action, processing, requires_capture, succeeded, failed, canceled] |

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
| **200** | Successfully retrieved payment intents |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="retrievePaymentIntent"></a>
# **retrievePaymentIntent**
> PaymentIntentResponseDto retrievePaymentIntent(id)

Retrieve Payment Intent

Retrieves the current state of a specific payment intent.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentIntentsApi apiInstance = new PaymentIntentsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment intent
    try {
      PaymentIntentResponseDto result = apiInstance.retrievePaymentIntent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentsApi#retrievePaymentIntent");
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
| **id** | **String**| The unique identifier of the payment intent | |

### Return type

[**PaymentIntentResponseDto**](PaymentIntentResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved payment intent |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

