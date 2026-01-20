# PurchasesApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPurchase**](PurchasesApi.md#createPurchase) | **POST** /api/canary/purchases | Buy with Cash Balance |


<a id="createPurchase"></a>
# **createPurchase**
> PurchaseResponseDto createPurchase(createPurchaseDto)

Buy with Cash Balance

(Wallet-Enabling) Spends a product using the CustomerBalance as the source. Atomically debits the CustomerBalance and credits the MerchantBalance.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.PurchasesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    PurchasesApi apiInstance = new PurchasesApi(defaultClient);
    CreatePurchaseDto createPurchaseDto = new CreatePurchaseDto(); // CreatePurchaseDto | Purchase details
    try {
      PurchaseResponseDto result = apiInstance.createPurchase(createPurchaseDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PurchasesApi#createPurchase");
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
| **createPurchaseDto** | [**CreatePurchaseDto**](CreatePurchaseDto.md)| Purchase details | |

### Return type

[**PurchaseResponseDto**](PurchaseResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Purchase created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **402** | Insufficient customer balance |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

