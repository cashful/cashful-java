# BalanceApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getBalanceHistory**](BalanceApi.md#getBalanceHistory) | **GET** /api/canary/balance/history | List Merchant Balance History |
| [**getMerchantBalance**](BalanceApi.md#getMerchantBalance) | **GET** /api/canary/balance | Get Merchant Balance |


<a id="getBalanceHistory"></a>
# **getBalanceHistory**
> BalanceHistoryResponseDto getBalanceHistory(merchantId, limit, offset, startDate, endDate, transactionType)

List Merchant Balance History

A full ledger of all transactions, fees, and payouts for the merchant&#39;s master account.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.BalanceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    BalanceApi apiInstance = new BalanceApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant. This parameter is required.
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal(78); // BigDecimal | Number of records to skip
    String startDate = "startDate_example"; // String | Filter transactions from this date (ISO 8601 format)
    String endDate = "endDate_example"; // String | Filter transactions until this date (ISO 8601 format)
    String transactionType = "transactionType_example"; // String | Filter by transaction type (e.g., \"credit\", \"debit\", \"fee\", \"payout\")
    try {
      BalanceHistoryResponseDto result = apiInstance.getBalanceHistory(merchantId, limit, offset, startDate, endDate, transactionType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BalanceApi#getBalanceHistory");
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
| **startDate** | **String**| Filter transactions from this date (ISO 8601 format) | [optional] |
| **endDate** | **String**| Filter transactions until this date (ISO 8601 format) | [optional] |
| **transactionType** | **String**| Filter by transaction type (e.g., \&quot;credit\&quot;, \&quot;debit\&quot;, \&quot;fee\&quot;, \&quot;payout\&quot;) | [optional] |

### Return type

[**BalanceHistoryResponseDto**](BalanceHistoryResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved balance history |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="getMerchantBalance"></a>
# **getMerchantBalance**
> MerchantBalanceResponseDto getMerchantBalance(merchantId)

Get Merchant Balance

Retrieves the merchant&#39;s own master balance (their earnings) available for payouts.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.BalanceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    BalanceApi apiInstance = new BalanceApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant whose balance is being requested.
    try {
      MerchantBalanceResponseDto result = apiInstance.getMerchantBalance(merchantId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BalanceApi#getMerchantBalance");
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
| **merchantId** | **String**| The ID of the merchant whose balance is being requested. | |

### Return type

[**MerchantBalanceResponseDto**](MerchantBalanceResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved merchant balance |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

