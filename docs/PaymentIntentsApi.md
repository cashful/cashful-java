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
> ConfirmPaymentIntentResponseDto confirmPaymentIntent(id, confirmPaymentIntentDto)

Confirm Payment Intent

Confirms a payment intent that requires confirmation and returns 3DS parameters for card authentication.

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
    ConfirmPaymentIntentDto confirmPaymentIntentDto = new ConfirmPaymentIntentDto(); // ConfirmPaymentIntentDto | 
    try {
      ConfirmPaymentIntentResponseDto result = apiInstance.confirmPaymentIntent(id, confirmPaymentIntentDto);
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
| **confirmPaymentIntentDto** | [**ConfirmPaymentIntentDto**](ConfirmPaymentIntentDto.md)|  | |

### Return type

[**ConfirmPaymentIntentResponseDto**](ConfirmPaymentIntentResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment intent confirmed and awaiting authentication |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="createPaymentIntent"></a>
# **createPaymentIntent**
> PaymentIntentResponseDto createPaymentIntent(createPaymentIntentDto)

Create Payment Intent

Creates a payment intent for a payment attempt. Used for hosted checkout or direct integrations.

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
> ListPaymentIntentsResponseDto listPaymentIntents(status, offset, limit, merchantId)

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
    String status = "initiation"; // String | 
    BigDecimal offset = new BigDecimal(78); // BigDecimal | 
    BigDecimal limit = new BigDecimal(78); // BigDecimal | 
    String merchantId = "merchantId_example"; // String | 
    try {
      ListPaymentIntentsResponseDto result = apiInstance.listPaymentIntents(status, offset, limit, merchantId);
      System.out.println(result);
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
| **status** | **String**|  | [optional] [enum: initiation, requires_payment_method, requires_confirmation, requires_action, processing, requires_capture, succeeded, failed, canceled] |
| **offset** | **BigDecimal**|  | [optional] |
| **limit** | **BigDecimal**|  | [optional] |
| **merchantId** | **String**|  | [optional] |

### Return type

[**ListPaymentIntentsResponseDto**](ListPaymentIntentsResponseDto.md)

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

