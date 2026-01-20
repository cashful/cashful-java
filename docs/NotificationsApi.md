# NotificationsApi

All URIs are relative to *https://api.cashful.africa*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**sendEmail**](NotificationsApi.md#sendEmail) | **POST** /api/canary/notifications/email | Send an email notification |
| [**sendMultiChannelNotification**](NotificationsApi.md#sendMultiChannelNotification) | **POST** /api/canary/notifications/multi-channel | Send notifications via multiple channels |
| [**sendNotification**](NotificationsApi.md#sendNotification) | **POST** /api/canary/notifications/send | Send a notification via specified channel |
| [**sendSms**](NotificationsApi.md#sendSms) | **POST** /api/canary/notifications/sms | Send an SMS notification |


<a id="sendEmail"></a>
# **sendEmail**
> SendEmail200Response sendEmail(sendEmailDto)

Send an email notification

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.models.*;
import com.cashful.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    SendEmailDto sendEmailDto = new SendEmailDto(); // SendEmailDto | 
    try {
      SendEmail200Response result = apiInstance.sendEmail(sendEmailDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#sendEmail");
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
| **sendEmailDto** | [**SendEmailDto**](SendEmailDto.md)|  | |

### Return type

[**SendEmail200Response**](SendEmail200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email sent successfully |  -  |
| **400** | Bad request |  -  |
| **500** | Failed to send email |  -  |

<a id="sendMultiChannelNotification"></a>
# **sendMultiChannelNotification**
> SendMultiChannelNotification200Response sendMultiChannelNotification()

Send notifications via multiple channels

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.models.*;
import com.cashful.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    try {
      SendMultiChannelNotification200Response result = apiInstance.sendMultiChannelNotification();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#sendMultiChannelNotification");
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

[**SendMultiChannelNotification200Response**](SendMultiChannelNotification200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notifications sent |  -  |

<a id="sendNotification"></a>
# **sendNotification**
> sendNotification(notificationDto)

Send a notification via specified channel

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.models.*;
import com.cashful.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    NotificationDto notificationDto = new NotificationDto(); // NotificationDto | 
    try {
      apiInstance.sendNotification(notificationDto);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#sendNotification");
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
| **notificationDto** | [**NotificationDto**](NotificationDto.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification sent successfully |  -  |
| **400** | Bad request |  -  |
| **500** | Failed to send notification |  -  |

<a id="sendSms"></a>
# **sendSms**
> SendSms200Response sendSms(sendSmsDto)

Send an SMS notification

### Example
```java
// Import classes:
import com.cashful.ApiClient;
import com.cashful.ApiException;
import com.cashful.Configuration;
import com.cashful.models.*;
import com.cashful.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.cashful.africa");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    SendSmsDto sendSmsDto = new SendSmsDto(); // SendSmsDto | 
    try {
      SendSms200Response result = apiInstance.sendSms(sendSmsDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#sendSms");
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
| **sendSmsDto** | [**SendSmsDto**](SendSmsDto.md)|  | |

### Return type

[**SendSms200Response**](SendSms200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | SMS sent successfully |  -  |
| **400** | Bad request |  -  |
| **500** | Failed to send SMS |  -  |

