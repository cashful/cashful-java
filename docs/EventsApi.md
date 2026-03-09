# EventsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createEvent**](EventsApi.md#createEvent) | **POST** /api/canary/events | Create Event |
| [**listEventTypes**](EventsApi.md#listEventTypes) | **GET** /api/canary/events/types | List Event Types |
| [**listEvents**](EventsApi.md#listEvents) | **GET** /api/canary/events | List Events |


<a id="createEvent"></a>
# **createEvent**
> createEvent(createEventDto)

Create Event

Records a new event and triggers associated webhooks.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.EventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    EventsApi apiInstance = new EventsApi(defaultClient);
    CreateEventDto createEventDto = new CreateEventDto(); // CreateEventDto | 
    try {
      apiInstance.createEvent(createEventDto);
    } catch (ApiException e) {
      System.err.println("Exception when calling EventsApi#createEvent");
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
| **createEventDto** | [**CreateEventDto**](CreateEventDto.md)|  | |

### Return type

null (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Event successfully created |  -  |

<a id="listEventTypes"></a>
# **listEventTypes**
> ListEventTypesResponseDto listEventTypes()

List Event Types

Retrieves all available event types that can be sent or subscribed to.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.EventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    EventsApi apiInstance = new EventsApi(defaultClient);
    try {
      ListEventTypesResponseDto result = apiInstance.listEventTypes();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EventsApi#listEventTypes");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListEventTypesResponseDto**](ListEventTypesResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved event types |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

<a id="listEvents"></a>
# **listEvents**
> ListEventsResponseDto listEvents(merchantId, limit, offset, filter, sort, order, type, status, startDate, endDate)

List Events

Retrieves a log of all API events for debugging and logging.

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.auth.*;
import com.cashful.models.*;
import com.cashful.api.EventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    EventsApi apiInstance = new EventsApi(defaultClient);
    String merchantId = "merchantId_example"; // String | The ID of the merchant whose events are being requested. This parameter is required.
    BigDecimal limit = new BigDecimal("50"); // BigDecimal | Maximum number of records to return
    BigDecimal offset = new BigDecimal("0"); // BigDecimal | Number of records to skip
    String filter = "{\"ids\":[\"prod_123\",\"prod_456\"]}"; // String | JSON string used for dynamic filtering
    String sort = "createdAt"; // String | Field name to sort by
    String order = "DESC"; // String | Sort direction (ASC or DESC)
    String type = "type_example"; // String | Filter by event type
    String status = "pending"; // String | Filter by event status
    String startDate = "startDate_example"; // String | Filter by start date
    String endDate = "endDate_example"; // String | Filter by end date
    try {
      ListEventsResponseDto result = apiInstance.listEvents(merchantId, limit, offset, filter, sort, order, type, status, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EventsApi#listEvents");
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
| **merchantId** | **String**| The ID of the merchant whose events are being requested. This parameter is required. | |
| **limit** | **BigDecimal**| Maximum number of records to return | [optional] |
| **offset** | **BigDecimal**| Number of records to skip | [optional] |
| **filter** | **String**| JSON string used for dynamic filtering | [optional] |
| **sort** | **String**| Field name to sort by | [optional] |
| **order** | **String**| Sort direction (ASC or DESC) | [optional] |
| **type** | **String**| Filter by event type | [optional] |
| **status** | **String**| Filter by event status | [optional] [enum: pending, delivered, failed] |
| **startDate** | **String**| Filter by start date | [optional] |
| **endDate** | **String**| Filter by end date | [optional] |

### Return type

[**ListEventsResponseDto**](ListEventsResponseDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved events |  -  |
| **400** | Bad Request - Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

