# ProductsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProduct**](ProductsApi.md#createProduct) | **POST** /api/canary/products | Create Product |
| [**deleteProduct**](ProductsApi.md#deleteProduct) | **DELETE** /api/canary/products/{id} | Delete Product |
| [**deleteProductsBulk**](ProductsApi.md#deleteProductsBulk) | **DELETE** /api/canary/products/bulk | Bulk Delete Products |
| [**listProducts**](ProductsApi.md#listProducts) | **GET** /api/canary/products | List Products |
| [**retrieveProduct**](ProductsApi.md#retrieveProduct) | **GET** /api/canary/products/{id} | Retrieve Product |
| [**updateProduct**](ProductsApi.md#updateProduct) | **PATCH** /api/canary/products/{id} | Update Product |
| [**updateProductsBulk**](ProductsApi.md#updateProductsBulk) | **PATCH** /api/canary/products/bulk | Bulk Update Products |


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

<a id="deleteProduct"></a>
# **deleteProduct**
> ProductResponseDto deleteProduct(id)

Delete Product

Deletes a product by ID.

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
      ProductResponseDto result = apiInstance.deleteProduct(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#deleteProduct");
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
| **200** | Product deleted successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="deleteProductsBulk"></a>
# **deleteProductsBulk**
> Object deleteProductsBulk(bulkIdsDto)

Bulk Delete Products

Deletes multiple products by ID.

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
    BulkIdsDto bulkIdsDto = new BulkIdsDto(); // BulkIdsDto | 
    try {
      Object result = apiInstance.deleteProductsBulk(bulkIdsDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#deleteProductsBulk");
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
| **bulkIdsDto** | [**BulkIdsDto**](BulkIdsDto.md)|  | |

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
| **200** | Products deleted successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listProducts"></a>
# **listProducts**
> ListProductsResponseDto listProducts(limit, offset, filter, sort, order, merchantId, active)

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
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of items to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of items to skip
    String filter = "{\"ids\":[\"prod_123\",\"prod_456\"]}"; // String | JSON string used for dynamic filtering
    String sort = "id"; // String | Field name to sort by
    String order = "DESC"; // String | Sort direction
    String merchantId = "merchantId_example"; // String | The ID of the merchant whose products are being requested. If not provided, the products of the authenticated merchant will be returned.
    Boolean active = true; // Boolean | Filter by active status
    try {
      ListProductsResponseDto result = apiInstance.listProducts(limit, offset, filter, sort, order, merchantId, active);
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
| **limit** | **BigDecimal**| Maximum number of items to return | [optional] |
| **offset** | **BigDecimal**| Number of items to skip | [optional] |
| **filter** | **String**| JSON string used for dynamic filtering | [optional] |
| **sort** | **String**| Field name to sort by | [optional] [enum: id, name, amount, currency, active, merchantId, createdAt, updatedAt] |
| **order** | **String**| Sort direction | [optional] |
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
| **400** | Bad Request - Invalid input |  -  |
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

<a id="updateProductsBulk"></a>
# **updateProductsBulk**
> Object updateProductsBulk(bulkUpdateProductsInputDto)

Bulk Update Products

Updates multiple products using a shared patch.

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
    BulkUpdateProductsInputDto bulkUpdateProductsInputDto = new BulkUpdateProductsInputDto(); // BulkUpdateProductsInputDto | 
    try {
      Object result = apiInstance.updateProductsBulk(bulkUpdateProductsInputDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#updateProductsBulk");
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
| **bulkUpdateProductsInputDto** | [**BulkUpdateProductsInputDto**](BulkUpdateProductsInputDto.md)|  | |

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
| **200** | Products updated successfully |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

