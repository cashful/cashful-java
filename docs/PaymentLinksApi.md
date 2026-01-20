# PaymentLinksApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPaymentLink**](PaymentLinksApi.md#createPaymentLink) | **POST** /api/canary/payment-links | Create Payment Link |
| [**listPaymentLinks**](PaymentLinksApi.md#listPaymentLinks) | **GET** /api/canary/payment-links | List Payment Links |
| [**retrievePaymentLink**](PaymentLinksApi.md#retrievePaymentLink) | **GET** /api/canary/payment-links/{id} | Retrieve Payment Link |
| [**updatePaymentLink**](PaymentLinksApi.md#updatePaymentLink) | **PATCH** /api/canary/payment-links/{id} | Update Payment Link |


<a id="createPaymentLink"></a>
# **createPaymentLink**
> PaymentLinkResponseDto createPaymentLink(createPaymentLinkDto)

Create Payment Link

Creates a re-usable hosted link. Can be used for: (1) Selling a product, or (2) as a \&quot;Pay-In\&quot; link for a customer.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentLinksApi apiInstance = new PaymentLinksApi(defaultClient);
    CreatePaymentLinkDto createPaymentLinkDto = new CreatePaymentLinkDto(); // CreatePaymentLinkDto | Payment link details
    try {
      PaymentLinkResponseDto result = apiInstance.createPaymentLink(createPaymentLinkDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentLinksApi#createPaymentLink");
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
| **createPaymentLinkDto** | [**CreatePaymentLinkDto**](CreatePaymentLinkDto.md)| Payment link details | |

### Return type

[**PaymentLinkResponseDto**](PaymentLinkResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Payment link created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="listPaymentLinks"></a>
# **listPaymentLinks**
> ListPaymentLinksResponseDto listPaymentLinks(merchantId, limit, offset, active)

List Payment Links

Retrieves all payment links created by the merchant.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentLinksApi apiInstance = new PaymentLinksApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant. This parameter is required.
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal(78); // BigDecimal | Number of records to skip
    Boolean active = true; // Boolean | Filter by active status
    try {
      ListPaymentLinksResponseDto result = apiInstance.listPaymentLinks(merchantId, limit, offset, active);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentLinksApi#listPaymentLinks");
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
| **active** | **Boolean**| Filter by active status | [optional] |

### Return type

[**ListPaymentLinksResponseDto**](ListPaymentLinksResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved payment links |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="retrievePaymentLink"></a>
# **retrievePaymentLink**
> PaymentLinkResponseDto retrievePaymentLink(id)

Retrieve Payment Link

Retrieves a single payment link by ID.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentLinksApi apiInstance = new PaymentLinksApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment link
    try {
      PaymentLinkResponseDto result = apiInstance.retrievePaymentLink(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentLinksApi#retrievePaymentLink");
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
| **id** | **String**| The unique identifier of the payment link | |

### Return type

[**PaymentLinkResponseDto**](PaymentLinkResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment link retrieved successfully |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="updatePaymentLink"></a>
# **updatePaymentLink**
> Object updatePaymentLink(id, updatePaymentLinkDto)

Update Payment Link

Updates a link&#39;s details, most commonly to set active: false.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PaymentLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PaymentLinksApi apiInstance = new PaymentLinksApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the payment link
    UpdatePaymentLinkDto updatePaymentLinkDto = new UpdatePaymentLinkDto(); // UpdatePaymentLinkDto | Payment link update details
    try {
      Object result = apiInstance.updatePaymentLink(id, updatePaymentLinkDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentLinksApi#updatePaymentLink");
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
| **id** | **String**| The unique identifier of the payment link | |
| **updatePaymentLinkDto** | [**UpdatePaymentLinkDto**](UpdatePaymentLinkDto.md)| Payment link update details | |

### Return type

**Object**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payment link updated successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

