# ProductsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProduct**](ProductsApi.md#createProduct) | **POST** /api/canary/products | Create Product |
| [**listProducts**](ProductsApi.md#listProducts) | **GET** /api/canary/products | List Products |
| [**retrieveProduct**](ProductsApi.md#retrieveProduct) | **GET** /api/canary/products/{id} | Retrieve Product |
| [**updateProduct**](ProductsApi.md#updateProduct) | **PATCH** /api/canary/products/{id} | Update Product |


<a id="createProduct"></a>
# **createProduct**
> ProductResponseDto createProduct(createProductDto)

Create Product

Defines a product in the merchant&#39;s catalog (e.g., \&quot;Airtime,\&quot; \&quot;Data\&quot;).

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    CreateProductDto createProductDto = new CreateProductDto(); // CreateProductDto | Product details
    try {
      ProductResponseDto result = apiInstance.createProduct(createProductDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#createProduct");
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
| **createProductDto** | [**CreateProductDto**](CreateProductDto.md)| Product details | |

### Return type

[**ProductResponseDto**](ProductResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product created successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

<a id="listProducts"></a>
# **listProducts**
> ListProductsResponseDto listProducts(limit, offset, merchantId, active)

List Products

Retrieves all products in the merchant&#39;s catalog.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of records to skip
    String merchantId = "merchantId_example"; // String | The ID of the merchant whose products are being requested. If not provided, the products of the authenticated merchant will be returned.
    Boolean active = true; // Boolean | Filter by active status
    try {
      ListProductsResponseDto result = apiInstance.listProducts(limit, offset, merchantId, active);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#listProducts");
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
| **merchantId** | **String**| The ID of the merchant whose products are being requested. If not provided, the products of the authenticated merchant will be returned. | [optional] |
| **active** | **Boolean**| Filter by active status | [optional] |

### Return type

[**ListProductsResponseDto**](ListProductsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved products |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="retrieveProduct"></a>
# **retrieveProduct**
> ProductResponseDto retrieveProduct(id)

Retrieve Product

Retrieves a single product by ID.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the product
    try {
      ProductResponseDto result = apiInstance.retrieveProduct(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#retrieveProduct");
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
| **id** | **String**| The unique identifier of the product | |

### Return type

[**ProductResponseDto**](ProductResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved product |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="updateProduct"></a>
# **updateProduct**
> ProductResponseDto updateProduct(id, updateProductDto)

Update Product

Updates a product&#39;s name, description, or metadata.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "id_example"; // String | The unique identifier of the product
    UpdateProductDto updateProductDto = new UpdateProductDto(); // UpdateProductDto | Product update details
    try {
      ProductResponseDto result = apiInstance.updateProduct(id, updateProductDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#updateProduct");
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
| **id** | **String**| The unique identifier of the product | |
| **updateProductDto** | [**UpdateProductDto**](UpdateProductDto.md)| Product update details | |

### Return type

[**ProductResponseDto**](ProductResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product updated successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

