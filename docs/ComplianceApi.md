# ComplianceApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCompliance**](ComplianceApi.md#createCompliance) | **POST** /api/canary/compliance | Create Compliance info |
| [**listCompliance**](ComplianceApi.md#listCompliance) | **GET** /api/canary/compliance | List Compliance info for organization |
| [**updateCompliance**](ComplianceApi.md#updateCompliance) | **PATCH** /api/canary/compliance/{id} | Update Compliance info |


<a id="createCompliance"></a>
# **createCompliance**
> OrganizationComplianceResponseDto createCompliance(createOrganizationComplianceDto)

Create Compliance info

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ComplianceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ComplianceApi apiInstance = new ComplianceApi(defaultClient);
    CreateOrganizationComplianceDto createOrganizationComplianceDto = new CreateOrganizationComplianceDto(); // CreateOrganizationComplianceDto | 
    try {
      OrganizationComplianceResponseDto result = apiInstance.createCompliance(createOrganizationComplianceDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ComplianceApi#createCompliance");
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
| **createOrganizationComplianceDto** | [**CreateOrganizationComplianceDto**](CreateOrganizationComplianceDto.md)|  | |

### Return type

[**OrganizationComplianceResponseDto**](OrganizationComplianceResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="listCompliance"></a>
# **listCompliance**
> ListOrganizationComplianceResponseDto listCompliance(limit, offset, filter, sort, order)

List Compliance info for organization

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ComplianceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ComplianceApi apiInstance = new ComplianceApi(defaultClient);
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of items to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of items to skip
    String filter = "{\"ids\":[\"prod_123\",\"prod_456\"]}"; // String | JSON string used for dynamic filtering
    String sort = "createdAt"; // String | Field name to sort by
    String order = "DESC"; // String | Sort direction
    try {
      ListOrganizationComplianceResponseDto result = apiInstance.listCompliance(limit, offset, filter, sort, order);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ComplianceApi#listCompliance");
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

### Return type

[**ListOrganizationComplianceResponseDto**](ListOrganizationComplianceResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="updateCompliance"></a>
# **updateCompliance**
> updateCompliance(id, updateOrganizationComplianceDto)

Update Compliance info

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ComplianceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ComplianceApi apiInstance = new ComplianceApi(defaultClient);
    String id = "id_example"; // String | 
    UpdateOrganizationComplianceDto updateOrganizationComplianceDto = new UpdateOrganizationComplianceDto(); // UpdateOrganizationComplianceDto | 
    try {
      apiInstance.updateCompliance(id, updateOrganizationComplianceDto);
    } catch (ApiException e) {
      System.err.println("Exception when calling ComplianceApi#updateCompliance");
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
| **id** | **String**|  | |
| **updateOrganizationComplianceDto** | [**UpdateOrganizationComplianceDto**](UpdateOrganizationComplianceDto.md)|  | |

### Return type

null (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Compliance updated |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

