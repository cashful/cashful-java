# CustomersApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCustomer**](CustomersApi.md#createCustomer) | **POST** /api/canary/customers | Create Customer |
| [**getCustomerBalance**](CustomersApi.md#getCustomerBalance) | **GET** /api/canary/customers/{id}/balance | Get Customer&#39;s Cash Balance |
| [**listCustomerPaymentMethods**](CustomersApi.md#listCustomerPaymentMethods) | **GET** /api/canary/customers/{id}/payment-methods | List Customer&#39;s Payment Methods |
| [**listCustomerTransactions**](CustomersApi.md#listCustomerTransactions) | **GET** /api/canary/customers/{id}/transactions | List Customer&#39;s Cash Transactions |
| [**listCustomers**](CustomersApi.md#listCustomers) | **GET** /api/canary/customers | List Customers |
| [**retrieveCustomer**](CustomersApi.md#retrieveCustomer) | **GET** /api/canary/customers/{id} | Retrieve Customer |
| [**updateCustomer**](CustomersApi.md#updateCustomer) | **PATCH** /api/canary/customers/{id} | Update Customer |


<a id="createCustomer"></a>
# **createCustomer**
> CustomerResponseDto createCustomer(createCustomerDto)

Create Customer

Creates a new customer object. This also provisions their \&quot;cash balance\&quot; feature (starting at 0).

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    CreateCustomerDto createCustomerDto = new CreateCustomerDto(); // CreateCustomerDto | Customer details
    try {
      CustomerResponseDto result = apiInstance.createCustomer(createCustomerDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#createCustomer");
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
| **createCustomerDto** | [**CreateCustomerDto**](CreateCustomerDto.md)| Customer details | |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Customer created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **409** | Customer with this email already exists |  -  |
| **500** | Internal server error |  -  |

<a id="getCustomerBalance"></a>
# **getCustomerBalance**
> CustomerBalanceDto getCustomerBalance(id)

Get Customer&#39;s Cash Balance

Retrieves the real-time balance for a single customer&#39;s \&quot;cash balance\&quot; (the \&quot;wallet-enabling\&quot; feature).

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the customer
    try {
      CustomerBalanceDto result = apiInstance.getCustomerBalance(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#getCustomerBalance");
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
| **id** | **String**| The unique identifier of the customer | |

### Return type

[**CustomerBalanceDto**](CustomerBalanceDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved customer&#39;s cash balance |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listCustomerPaymentMethods"></a>
# **listCustomerPaymentMethods**
> ListCustomerPaymentMethodsResponseDto listCustomerPaymentMethods(id, limit, offset)

List Customer&#39;s Payment Methods

Shows all saved payment methods (cards, etc.) for a single customer.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the customer
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal(78); // BigDecimal | Number of records to skip
    try {
      ListCustomerPaymentMethodsResponseDto result = apiInstance.listCustomerPaymentMethods(id, limit, offset);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#listCustomerPaymentMethods");
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
| **id** | **String**| The unique identifier of the customer | |
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] |

### Return type

[**ListCustomerPaymentMethodsResponseDto**](ListCustomerPaymentMethodsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved customer&#39;s payment methods |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listCustomerTransactions"></a>
# **listCustomerTransactions**
> ListCustomerTransactionsResponseDto listCustomerTransactions(id, limit, offset)

List Customer&#39;s Cash Transactions

Provides the full transaction history for a single customer&#39;s \&quot;cash balance\&quot; (Pay-Ins, Purchases, Transfers).

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the customer
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal(78); // BigDecimal | Number of records to skip
    try {
      ListCustomerTransactionsResponseDto result = apiInstance.listCustomerTransactions(id, limit, offset);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#listCustomerTransactions");
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
| **id** | **String**| The unique identifier of the customer | |
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] |

### Return type

[**ListCustomerTransactionsResponseDto**](ListCustomerTransactionsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved customer transactions |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listCustomers"></a>
# **listCustomers**
> ListCustomersResponseDto listCustomers(merchantId, limit, offset, email, search)

List Customers

Retrieves a paginated list of all customers for the merchant.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant. This parameter is required.
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal(78); // BigDecimal | Number of records to skip
    String email = "email_example"; // String | Filter by email address
    String search = "search_example"; // String | Search across customer fields
    try {
      ListCustomersResponseDto result = apiInstance.listCustomers(merchantId, limit, offset, email, search);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#listCustomers");
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
| **email** | **String**| Filter by email address | [optional] |
| **search** | **String**| Search across customer fields | [optional] |

### Return type

[**ListCustomersResponseDto**](ListCustomersResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved customers list |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="retrieveCustomer"></a>
# **retrieveCustomer**
> CustomerResponseDto retrieveCustomer(id)

Retrieve Customer

Gets the details for a single customer.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the customer
    try {
      CustomerResponseDto result = apiInstance.retrieveCustomer(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#retrieveCustomer");
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
| **id** | **String**| The unique identifier of the customer | |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved customer details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="updateCustomer"></a>
# **updateCustomer**
> CustomerResponseDto updateCustomer(id, updateCustomerDto)

Update Customer

Updates a customer&#39;s details (e.g., email, metadata).

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the customer
    UpdateCustomerDto updateCustomerDto = new UpdateCustomerDto(); // UpdateCustomerDto | Customer update details
    try {
      CustomerResponseDto result = apiInstance.updateCustomer(id, updateCustomerDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#updateCustomer");
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
| **id** | **String**| The unique identifier of the customer | |
| **updateCustomerDto** | [**UpdateCustomerDto**](UpdateCustomerDto.md)| Customer update details | |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Customer updated successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **409** | Email already in use by another customer |  -  |
| **500** | Internal server error |  -  |

