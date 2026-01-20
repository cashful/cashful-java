# PayoutsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPayout**](PayoutsApi.md#createPayout) | **POST** /api/canary/payouts | Create Payout |
| [**listPayouts**](PayoutsApi.md#listPayouts) | **GET** /api/canary/payouts | List Payouts |


<a id="createPayout"></a>
# **createPayout**
> PayoutResponseDto createPayout(createPayoutDto)

Create Payout

Allows the merchant to move funds from their MerchantBalance (their earnings) to their external bank account.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    CreatePayoutDto createPayoutDto = new CreatePayoutDto(); // CreatePayoutDto | Payout details
    try {
      PayoutResponseDto result = apiInstance.createPayout(createPayoutDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#createPayout");
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
| **createPayoutDto** | [**CreatePayoutDto**](CreatePayoutDto.md)| Payout details | |

### Return type

[**PayoutResponseDto**](PayoutResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Payout created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **402** | Insufficient merchant balance |  -  |
| **500** | Internal server error |  -  |

<a id="listPayouts"></a>
# **listPayouts**
> ListPayoutsResponseDto listPayouts(merchantId, limit, offset, status)

List Payouts

Retrieves a list of all historical and pending payouts for the merchant.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant. This parameter is required.
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal(78); // BigDecimal | Number of records to skip
    String status = "status_example"; // String | Filter by status
    try {
      ListPayoutsResponseDto result = apiInstance.listPayouts(merchantId, limit, offset, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#listPayouts");
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
| **status** | **String**| Filter by status | [optional] |

### Return type

[**ListPayoutsResponseDto**](ListPayoutsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved payouts |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

